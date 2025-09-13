Created on: 06-09-2025 16:34, note by Youssef Okeil
Status: #idea
Tags: #debugging #research
# Debugging Report

## 1) Compilation Issues:
- using only one `<` before `cout`, should be `cout <<` & `<< endl`
	![[Pasted image 20250906164409.png]]
- only one `/` when trying to make a comment -> should be `//`
	![[Pasted image 20250906164739.png]]
	![[Pasted image 20250906170017.png]]
-  CMAKE bug as the `target_link_libraries()` was commented, also it should be `target_link_libraries(debug_challenge Eigen3::Eigen)` instead of `target_link_libraries(debug_challenge Eigen3: Eigen)`.  
	"Items containing `::`, such as `Foo::Bar`, are assumed to be [IMPORTED](https://cmake.org/cmake/help/latest/manual/cmake-buildsystem.7.html#imported-targets) or [ALIAS](https://cmake.org/cmake/help/latest/manual/cmake-buildsystem.7.html#alias-targets) library target names and will cause an error if no such target exists. See policy [`CMP0028`](https://cmake.org/cmake/help/latest/policy/CMP0028.html#policy:CMP0028 "CMP0028")." For more visit https://cmake.org/cmake/help/latest/command/target_link_libraries.html.
	![[Pasted image 20250906165730.png]]
- Missing a header `#include <Eigen/Dense>`, for more visit https://libeigen.gitlab.io/eigen/docs-nightly/GettingStarted.html. You need to install eigen on your device first!
- For type aliases like `Eigen: Vector3d`, it should be written as `Eigen::Vector3d`
	![[Pasted image 20250906172151.png]]
- Missing an extra `+` in the for loop --> should be `i++`
	![[Pasted image 20250906173109.png]]
- "CMakeList BUG" should be commented
	![[Pasted image 20250906173403.png]]
- Comma initialization for the rotation matrix is not correct. should be `rotation<<` before the values. For more visit https://libeigen.gitlab.io/eigen/docs-nightly/group__TutorialAdvancedInitialization.html.
--------------
## 2) String Decoding Logic
- from my understanding the string decoding logic takes numbers and extracts the corresponding ASCII values. The logic may cause a problem if values are > 127, which the if conditional doesn't check. so I'll add `&& values[i] < 127`
- also `values[i]>0`, doesn't make a lot of sense. Because a lot of the first values are things that we can't read properly, see the figure below. So I changed the logic to `values[i] >= 32 && values[i] < 127`, and I print an out of range message when it is not in that range. 
	![[Pasted image 20250906181532.png]]
	shows that the `decodeMessage(int, int)` function got passed values that can't be readable for us. 
	
	![[Pasted image 20250906181324.png|500]]
-------------------
## 3) Rotation Matrix Transformation
- Rotation matrix doesn't seem to match any rotation around any of the primary axes. See figure below. I'll assume that the rotation is around z- Axis, if this is true then it should be.
	**NB: this is assuming the standard counter-clockwise rotation.**
$$
rotation = \begin{pmatrix} cos(\theta) & -sin(\theta) & 0 \\ sin(\theta) & cos(\theta) & 0 \\ 0 & 0  &  1\end{pmatrix}
$$ 


$$old\_rotation = \begin{pmatrix} cos(\theta) & sin(\theta) & 0 \\ -sin(\theta) & cos(\theta) & 0 \\ 0 & 0  &  1\end{pmatrix}

$$

![[Pasted image 20250906181915.png]]
*from ResearchGate*

-----------------
<br>
<br>
<br>
<br><br><br>


# References
1. https://wow2006.github.io/posts/beginner-guide-to-using-eigen3-cmake-cpp/
2. https://libeigen.gitlab.io/eigen/docs-nightly/group__TutorialAdvancedInitialization.html
3. https://libeigen.gitlab.io/eigen/docs-nightly/GettingStarted.html
4. https://cmake.org/cmake/help/latest/command/target_link_libraries.html
5. https://www.researchgate.net/figure/Definition-of-the-rotation-matrices-trough-the-axis-x-y-and-z-taken-from-Meyer-2000_fig3_237030100
6. https://commons.wikimedia.org/wiki/File:ASCII-Table-wide.svg