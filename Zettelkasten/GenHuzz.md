Created on: 12-10-2025 10:59, note by Youssef Okeil
Status: #idea
Tags: #paper_review 
# GenHuzz
## Background 
- **Fuzzing:** involves generating and mutating random test cases, monitoring the DUT, and analyzing for vulnerabilities. 
	**traditional fuzzing:**
	- generates random test cases, monitoring the DUT.
	- uses mutation algorithms to create new test cases. 
	- the test cases are the fed to the DUT, status is monitored and crashes are recorded.
	fuzzing is classified into black-box fuzzing, grey-box fuzzing and white-box fuzzing.
	**white-box fuzzing:**
	- comprehensive knowledge about data flow, control flow, data format, protocols and high-level architecture. 
	- maximum code coverage through feedback engines. 
## Hardware fuzzing Challenges:
1. fuzzer should understand interdependencies between instructions to trigger vulnerabilities and bugs that hide in the DUT
	- current approaches solely focus on basic instruction mutations
	- multiple instructions combinations are undetected
2. existing fuzzers have *low feedback utilization*, feedback serves only to discard ineffective test cases
	- discard ineffective test cases rather than inform the generation of better ones
	- coverage plateaus quickly, leaving some vulnerabilities unexplored
3. Requires a large number of test cases to detect vulnerabilities
## Contributions of the paper:
- employs a novel approach by framing hardware fuzzing as an optimization problem.
- fuzzing policy is dynamically adjusted through RL guided by hardware feedback
1. uses a language model-based fuzzer instead of conventional fuzzers that rely on mutations and instruction rules. It comprehends the semantics of instructions
2. Hardware-Guided RL, fine-tunes the fuzzing policy on real-time hardware coverage feedback. 
3. it is tested on different RISC-V cores without need to adapt GenHuzz
4. **Findings:**
	- identified 10 previously unreported bugs and vulnerabilities.
	- from the 10 vulnerabilities, there were 5 vulnerabilities with high severity scores exceeding 7.3/10
	- Tested the older versions of benchmark cores and successfully triggered all previous bugs.
##  GenHuzz:
employs a teacher-student framework, where the DUT --> teacher, fuzzer --> student. 
1. fuzzer initialization:
	grasp the fundamental rules of assembly instructions. this allows it to generate highly accurate and adaptable random assembly instructions.
	should understand both:
	- *intra-instruction semantics:* how to generate valid individual instructions
	- *inter-instruction semantics:* combine multiple instructions to uncover more complex bugs and vulnerabilities
2. HGRL
	learns the fuzzing policy, by understanding the semantics of the test cases. Feedback is driven by a reward system designed to accurately reflect hardware's behaviour and encourage fuzzer to generate test cases. 
3. vulnerability detection
	execution logs from the DUT and the Goldern Reference Model are compared to detect bugs. 

## Technical Details:
1. **fuzzer initialization:**
	1. concatenation of assembly instructions into a single sequence with separations.
	2. Each instruction $I_i$ is tokenized into k tokens
	3. tokens are encoded to prepare it for training the model.
	4. The loss function is cross-entropy loss.
	5. utilize gradient descent to minimize loss function
2. **Reinforcement Learning:**
	there is a problem that reward should be assigned to each action (token) as the action changes the state. However, when an action is part of an instruction is challenging, because;
	- only a complete instruction will be rewarded, thus reward for action will be delayed.
	- not all instructions are executed (think of branching)
	- a correct instruction can cause exceptions when executing on the DUT.

---------------
# References