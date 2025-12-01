---
kindle-sync:
  bookId: '17157'
  title: Deep Learning for EEG Based Brain-Computer Interfaces
  author: Xiang Zhang
  highlightsCount: 300
---
# Deep Learning for EEG Based Brain-Computer Interfaces
## Metadata
* Author: [[Xiang Zhang]]

## Highlights
One big challenge obstructing your superpower is the ineffectiveness and inaccuracy of brain signal decoding. — location: [32]() ^ref-42076

---
BCI including robust brain signal representation learning, cross-scenario classification, and semi-supervised classification. — location: [39]() ^ref-21512

---
ordinary individuals can enjoy enhanced entertainment and security when brain waves–based techniques are involved (Zhang et al., 2018g). — location: [195]() ^ref-64902

---
comprised of five key components: brain signal collection, signal preprocessing, feature engineering, and smart equipment. — location: [200]() ^ref-21007

---
For example, collection of EEG signals, which measure the voltage fluctuation resulting from ionic current within the neurons of the brain, requires placing a series of electrodes on to the scalp to record the electrical brain activity. — location: [206]() ^ref-4332

---
ionic current generated within the brain is measured at the scalp, intervening matter (e.g., the skull) greatly decrease the signal quality. — location: [208]() ^ref-61007

---
The preprocessing component comprises multiple steps such as signal cleaning (e.g., smoothing the noisy signals or resolving the inconsistencies), signal normalization — location: [209]() ^ref-49259

---
(e.g., normalizing each channel of the signals along the time axis), signal enhancement (e.g., removing direct current), and signal reduction (presenting a reduced representation of the signal). — location: [210]() ^ref-58849

---
Feature engineering refers to the process of extracting discriminating features from the input signals using domain knowledge. Traditional features are extracted from the time domain (e.g., variance, mean value, kurtosis), frequency domain (e.g., fast Fourier transform), and time– frequency domains (e.g., discrete wavelet transform), and analyzed to enrich distinguishable information regarding user intention. — location: [212]() ^ref-15702

---
Recent studies have shown deep learning algorithms to be more powerful than traditional classifiers. — location: [219]() ^ref-51232

---
The low SNR cannot be easily addressed by traditional methods due to the time they require and the accompanying risk of information loss (Zhang et al., 2018h). — location: [224]() ^ref-17981

---
General life experience may prove helpful in certain aspects but fall short overall. — location: [228]() ^ref-64405

---
Second, manual feature engineering is highly dependent on human expertise in the relevant domain. — location: [226]() ^ref-50279

---
Third, most existing machine learning research focuses on static data and therefore, cannot accurately classify rapidly changing brain signals. — location: [230]() ^ref-25059

---
Furthermore, in practice, the annotated brain signal samples are not easily obtained, because such labeling requires a large number of certified labelers with professional knowledge. — location: [233]() ^ref-23852

---
Deep learning can learn high-level and complicated representations by combining a number of simpler representations while each simple representation extracts partial information relating to the complex representation. — location: [238]() ^ref-52533

---
In other words, deep learning can learn high-quality representations even though the input is corrupted and noisy. — location: [244]() ^ref-1505

---
Discriminative deep learning models, which classify the input data into a preknown label based on the adaptively learned discriminative features. — location: [528]() ^ref-12461

Supervised learning

---
Discriminative architectures mainly include Multilayer Perceptron (MLP), Recurrent Neural Networks (RNN), Convolutional Neural Networks (CNN), along with their variations. — location: [532]() ^ref-62428

---
Representative deep learning models, which learn the pure and representative features from the input data. These algorithms only have the function of feature engineering (corresponding to Figure 1.1) but fail to classify. — location: [538]() ^ref-61976

---
autoencoder (AE), restricted Boltzmann machine — location: [540]() ^ref-41808

---
(RBM), deep belief networks (DBN), along with their variations. — location: [540]() ^ref-4446

---
Generative deep learning models, which learn the joint probability distribution of the input data and the target label. In the brain signal scope, generative algorithms are mostly used to reconstruct or generate a batch of brain signal samples to enhance the training set. — location: [541]() ^ref-39403

---
Almost all the classification functions in neural networks are implemented by a softmax layer, which will not be regarded as an algorithmic component. — location: [548]() ^ref-15149

---
observations — location: [557]() ^ref-10788

Features

---
the discriminative models receive the input data and output the corresponding category or label. — location: [558]() ^ref-61537

---
The term “fully connected” denotes that each node in a specific layer is connected with all the nodes in the previous and next layers. — location: [569]() ^ref-3713

---
Generally, ANN represents neural networks with fewer hidden layers (shallow), whereas DNN has more (in this case, DNN is equivalent to MLP). — location: [588]() ^ref-26128

---
input It but also the hidden state of the previous node ct−1. — location: [594]() ^ref-27319

---
They both follow the basic principles of RNN, and we will pay attention to the complicated internal structures in each node. — location: [597]() ^ref-37119

---
In this way, LSTM is empowered to remember important information in the time domain. — location: [612]() ^ref-52562

---
control the memory of specific information. — location: [613]() ^ref-46202

---
LSTM cell adopts four gates: the input gate, forget gate, output gate, and input modulation gate. — location: [613]() ^ref-40566

---
Another widely used RNN architecture is GRU. Similar to LSTM, GRU attempts to exploit the information from the past. — location: [631]() ^ref-366

---
reset gate r and update gate z. The former decides how to combine the input with previous memory. The latter decides how much of its previous memory to keep around, — location: [635]() ^ref-9022

---
It can be observed that there’s an intermediate variable  which is similar to the hidden state of LSTM. — location: [640]() ^ref-47410

---
which provides better performance. Second, GRU — location: [643]() ^ref-15468

---
GRU is lightweight because it only has two gates and no hidden state. — location: [643]() ^ref-8271

---
GRU costs less training time and requires less data for generalization. In contrast, LSTM generally works better if the training data set is big enough. — location: [644]() ^ref-53373

---
object searching due to their salient features such as regularized structure, good spatial locality, and translation invariance. — location: [648]() ^ref-55165

---
CNN is supposed to capture the distinctive dependencies among the patterns associated with different brain signals. — location: [649]() ^ref-39360

---
The pooling layer aims to reduce the spatial size of the features progressively. — location: [657]() ^ref-21796

---
CNN is the most popular deep learning model in brain signal research, which can be used to exploit the latent spatial dependencies among input brain signals like fMRI, spontaneous EEG, and so on. — location: [661]() ^ref-40831

---
The representative models including AE, RBM,5 and DBN are unsupervised learning methods. — location: [665]() ^ref-24261

---
Thus, they can learn the representative features from only the input observations x without the ground truth . — location: [666]() ^ref-28303

---
AE contains three layers where the input layer and the output layer are supposed to have the same values. — location: [674]() ^ref-16373

---
stacked AE has more than one hidden layer. Generally, the number of hidden layers is odd, and the middle layer is the learned representative features. — location: [676]() ^ref-2989

---
deep-RBM has one visible layer and multiple hidden layers, the last layer is the encoded representation. — location: [677]() ^ref-50564

---
Thus, D-AE generally has an odd number of hidden layers (e.g., 2n + 1), where the first n layers belong to the encoder, the (n + 1)-th layer works as the code that belongs to both encoder and decoder, and the last n layers belong to the decoder. — location: [690]() ^ref-19517

---
Deep-AE (D-AE) — location: [688]() ^ref-10589

---
Here only the D-AE is introduced because it is easily confused with the AE-based DBN. — location: [698]() ^ref-32937

---
xh (generally the code layer has lower dimension) and then reconstructing the data based on the code. — location: [700]() ^ref-4057

---
x into a code — location: [700]() ^ref-56978

---
If the reconstructed y′ can approximate the input data x, it can be demonstrated that the condensed code xh carries enough information about x; thus, xh can be considered a representation of the input data for future operation (e.g., classification). — location: [701]() ^ref-9788

---
visible layer (input layer) and one hidden layer, as shown in Figure 3.5(b). From the figure, we can see that the connection lines between the two layers are bidirectional. — location: [706]() ^ref-12642

---
The first step condenses the input data from the original space to the hidden layer in a latent space. — location: [709]() ^ref-3156

---
that the Deep-RBM (D-RBM) is an RBM with multiple hidden layers. — location: [715]() ^ref-32693

---
which is composed of AE, and DBN-RBM (also called stacked RBM), which is composed of RBM. — location: [719]() ^ref-3106

---
DBN-AE (also called stacked AE), which is composed of AE, and DBN-RBM (also called stacked RBM), which is composed of RBM. — location: [718]() ^ref-42794

---
This iteration continues until the AE converges. We get the mapping: x1 → xh1. — location: [723]() ^ref-30894

---
Then, in the second stage, the learned representative code in the hidden layer xh1 will be used as the input layer of the second AE, — location: [724]() ^ref-32590

---
While DBN-RBM and D-RBM (Figure 3.5(d)) have similar architecture, the former is trained greedily while the latter is trained jointly. — location: [730]() ^ref-2293

---
xh2 denotes the hidden layer of the second AE, meanwhile, it is the final outcome of the DBN-AE. — location: [733]() ^ref-20452

---
The most important difference between the DBN and the deep AE/RBM is that the former is trained greedily, whereas the latter is trained jointly. — location: [739]() ^ref-36859

---
In particular, for the DBN, the first AE/RBM is trained first, after it converges, the second AE/RBM is trained (Hinton and Salakhutdinov, 2006). For the deep AE/RBM, joint training means that the whole structure is trained together, no matter how many layers it has. — location: [740]() ^ref-51610

---
generative deep learning models play a supporting role in the brain signal field to enhance the training data quality and quantity. — location: [744]() ^ref-49643

---
In this section, two typical generative deep learning models, VAE and GAN, will be introduced. — location: [747]() ^ref-41817

---
The standard AE and its other variants can be used for representation but fail in generation for the reason that the learned code (or representation) may not be continuous. — location: [750]() ^ref-44659

---
In other words, the standard AE does not allow interpolation. — location: [751]() ^ref-32691

---
However, the learned representation in the latent space is forced to approximate a prior distribution  which is generally set as standard Gaussian distribution. — location: [756]() ^ref-47192

---
expectation μ and another denotes the standard deviation σ, — location: [758]() ^ref-49967

---
Then, the latent code in the hidden layer is not directly calculated but sampled from a Gaussian distribution (μ, σ2). The statistic code — location: [760]() ^ref-41888

---
where  The representation z is forced to a prior distribution, and the distance errorKL is measured by Kullback–Leibler divergence, — location: [763]() ^ref-8088

---
denotes the prior distribution. In the decoder, z is decoded into the output y′, — location: [765]() ^ref-47881

---
The overall error for VAE is combined by the DL divergence and the reconstruction error, — location: [768]() ^ref-55476

---
Thus, a representation z′ can be randomly sampled from the prior distribution and then a sample based on z′ can be reconstructed. — location: [771]() ^ref-21510

---
GAN (Goodfellow et al., 2014) was proposed in 2014 and has achieved great success in a wide range of research areas (e.g., computer vision and natural language processing). — location: [773]() ^ref-25029

---
The generator aims to generate fake samples, whereas the discriminator aims to distinguish whether the sample is genuine. — location: [776]() ^ref-40820

---
The functions of the generator and the discriminator are opposed; that’s why GAN is called “adversarial.” After the convergence of both the generator and the discriminator, the discriminator ought to be unable to recognize the generated samples. Thus, the pretrained generator can be used to create a batch of samples and use them for further operations such as as classification. Figure 3.7(b) shows the procedure of a standard GAN. The generator receives a noise signal s, which is randomly sampled from a multimodal Gaussian distribution and outputs the fake brain signals xF. The discriminator receives the real brain signals xR and the generated fake sample xF, and then it predicts whether the received sample is real or fake. The internal architectures of the generator and discriminator — location: [777]() ^ref-10383

---
After the convergence of both the generator and the discriminator, the discriminator ought to be unable to recognize the generated samples. — location: [778]() ^ref-21748

---
The generator receives a noise signal s, which is randomly sampled from a multimodal Gaussian distribution and outputs the fake brain signals xF — location: [780]() ^ref-13564

---
The discriminator receives the real brain signals xR and the generated fake sample xF, and then it predicts whether the received sample is real or fake. — location: [782]() ^ref-48828

---
After the convergence, numerous brain signals xG can be created by the generator. — location: [785]() ^ref-15079

---
ϵ denotes the standard normal distribution. — location: [790]() ^ref-53136

---
brain research, GAN reconstructs or augments data instead of classification. — location: [793]() ^ref-48316

---
Antoniades et al. (2016) employed CNN with two convolutional layers to extract features from epileptic intracortical data for detecting interictal epileptic discharge (IED). They sliced the input data into 80 ms segments with 40 ms overlapping windows and achieved an accuracy of about 87.51%. — location: [826]() ^ref-7373

---
wakefulness, non-REM 1, non-REM 2, slow wave sleep (SWS), and REM. — location: [848]() ^ref-6765

---
example, Vilamala et al. (2017) manually extracted the time–frequency features and achieved a classification accuracy of 86%. — location: [852]() ^ref-32819

---
Discriminative models. CNN are frequently used for sleep stage classification on single-channel EEG — location: [851]() ^ref-4223

---
Tan et al. (2015a) adopted a DBN-RBM algorithm to detect sleep spindle based on PSD features extracted from sleep EEG signals and achieved an F1 of 92.78% on a local data set. — location: [859]() ^ref-6434

---
Manzano et al. (2017) proposed a multiview algorithm in order to predict sleep stage by combining CNN and MLP. The CNN was employed to receive the raw time-domain EEG oscillations, whereas the MLP received the spectrum signals of 0.5–32 Hz obtained by the Short-Time Fourier Transform (STFT). — location: [861]() ^ref-43966

---
Deep learning models have been shown to be superior in the classification of EEG and real-motor EEG (Hartmann et al., 2018; Nurse et al., 2016). — location: [869]() ^ref-15447

---
Discriminative models. Such models mostly use CNN to classify MI EEG (Zhang et al., 2019b). — location: [870]() ^ref-23012

---
Others also used CNN for feature engineering — location: [873]() ^ref-33218

---
first used CNN to capture latent connections from MI EEG signals and then applied weak classifiers to choose important features for the final classification; — location: [874]() ^ref-32540

---
DBN is widely used as a basis for MI EEG classification for its high representative ability — location: [878]() ^ref-34759

---
extracted high-level representations from the time–frequency domain and location information of EEG signals using CNN and then applied a DBN-AE — location: [887]() ^ref-25440

---
with seven AEs as the classifier; Tan et al. (2017) used a denoising AE for — location: [888]() ^ref-29813

---
ERD/ERS refers to the phenomena that the magnitude and frequency distribution of the EEG signal power changes during a specific brain state (Huang et al., 2012). — location: [891]() ^ref-46279

---
ERD denotes the power decrease of ongoing EEG signals whereas ERS represents the power increase of EEG signals. — location: [892]() ^ref-2921

---
In most situations, ERD/ERS is regarded as a specific feature of the EEG powers for further analysis (Dai — location: [896]() ^ref-49788

---
(Pe − Pb)/Pb, where Pe denotes the signals’ power over a one-second segment while the event occurring and Pb denotes the signal power in a one-second segment during baseline which is before the event — location: [898]() ^ref-21909

---
DBN, especially DBN-RBM, is widely used in the unsupervised representation learning for emotion recognition — location: [913]() ^ref-935

---
The females’ results showed higher EEG signal diversity for the fearful emotion, whereas the males varied more for sadness. — location: [921]() ^ref-20375

---
Using a CNN structure, Morabito et al. (2016) tried to extract suitable features of multichannel EEG signals to distinguish patients with Alzheimer’s disease from patients with mild cognitive impairment and age-matched healthy controls. — location: [939]() ^ref-42335

---
Some models used dimensionality reduction methods such as PCA for preprocessing of the EEG signal — location: [950]() ^ref-706

---
It has been proposed that the generative models such as GAN could be used for data augmentation in brain signal classification (Abdelfattah et al., 2018). — location: [964]() ^ref-18454

---
An LSTM layer was employed to extract the latent features from the EEG signals, and the extracted features were input into a GAN structure. — location: [969]() ^ref-5020

---
After the augmentation, classification accuracy increased dramatically from 48% to 82%. — location: [972]() ^ref-37259

---
The authors demonstrated that GAN outperforms both AE and VAE. — location: [972]() ^ref-40773

---
After that, the authors exploited convolutional AE for representation learning and CNN — location: [978]() ^ref-37075

---
EEG could be used to distinguish the user’s mental state (logical versus emotional) — location: [983]() ^ref-25242

---
A few researchers have tried to establish a common framework which could be used for multiple BCI paradigms. Lawhern et al. (2018) — location: [1018]() ^ref-22888

---
(1) the hardware has higher portability with much lower price; — location: [427]() ^ref-28557

---
(2) the temporal resolution is very high — location: [428]() ^ref-16780

---
(3) EEG is relatively tolerant of subject movement and artifacts — location: [429]() ^ref-20630

---
(4) the subject doesn’t need to be exposed to high-intensity (>1 Tesla) magnetic fields. Thus, EEG can serve subjects that have — location: [429]() ^ref-51639

---
EPs can be split into event-related potentials (ERPs) and steady-state evoked potentials (SSEP) — location: [433]() ^ref-1312

---
Generally, when we talk about the term “EEG,” we refer to spontaneous EEG, which measures the brain signals under a specific state without external stimulation. — location: [438]() ^ref-57534

---
signals while the user is sleeping, undertaking a mental task (e.g., counting), under fatigue stage, suffering brain disorders, undertaking motor imagery tasks, and so on. — location: [439]() ^ref-848

---
BCI systems based on spontaneous EEG are challenging to train, because of the lower SNR and the larger — location: [444]() ^ref-15763

---
EP or evoked responses refer to EEG signals which are evoked by a event stimulus instead of spontaneously. — location: [446]() ^ref-55730

---
In contrast to spontaneous EEG, EP generally has higher amplitude and lower frequency. — location: [447]() ^ref-56656

---
ERP records the EEG signals in response to an isolated discrete stimulus event. — location: [449]() ^ref-23215

---
The stimuli frequency of ERP is generally lower than 2Hz. — location: [451]() ^ref-59424

---
SSEP is generated in response to a periodic stimulus at a fixed rate. The stimuli frequency of SSEP generally ranges within 3.5–75Hz. — location: [452]() ^ref-28958

---
visual evoked potentials (VEP); auditory evoked potentials (AEP); and somatosensory evoked potentials (SEP) (Cecotti — location: [454]() ^ref-10289

---
VEP. VEPs are a specific category of ERP caused by visual stimulus — location: [456]() ^ref-16242

---
There is a specific item (called the target) that separates from the rest of the other items (called distracters). — location: [461]() ^ref-50755

---
Nowadays, brain signal research mainly focuses on the static mode RSVP. — location: [464]() ^ref-10633

---
AEP. AEPs are a specific subclass of ERP in which responses to auditory (sound) — location: [465]() ^ref-24510

---
The most common AEP measured is the auditory brainstem response that is often employed to test the hearing ability of newborns and infants. — location: [466]() ^ref-44062

---
SEP.7 SEP is another commonly used subcategory of ERP, which is elicited by electrical stimulation of the peripheral nerves. — location: [470]() ^ref-11040

---
Thus, P300 denotes the positive potential of ERP waveform at approximately 300 ms after the presented stimuli. — location: [479]() ^ref-44605

---
The capital character P/N represents positive/negative electrical potentials. — location: [478]() ^ref-62111

---
In the oddball paradigm, the subject receives a series of stimuli where low-probability target items are mixed with high-probability nontarget items. — location: [483]() ^ref-37856

Is that based on informmation theory

---
SSEPs are another subcategory of EPs, which are periodic cortical responses evoked by certain repetitive stimuli with a constant frequency. — location: [494]() ^ref-46007

---
(e.g., a flickering light with fixed frequency). Technically, SSEP is defined as a form of response to repetitive sensory stimulation in which the constituent frequency components of the response remain constant over time in both amplitude and phase (Regan, 1977). — location: [496]() ^ref-55165

---
steady-state visually evoked potentials (SSVEP), steady-state auditory evoked potentials (SSAEP), and steady-state somatosensory evoked potentials (SSSEP). — location: [498]() ^ref-41116

---
In the brain signal area, most studies are focused on visual evoked steady potentials, and papers only rarely focus on auditory and somatosensory stimuli. — location: [499]() ^ref-54744

---
VEP, RSVP, and SSVEP. — location: [503]() ^ref-35431

---
frequency of SSVEP ranges from 3.5 to 75Hz. — location: [504]() ^ref-11247

---
In an RSVP diagram, several items will be presented on a screen one by one. All the items are shown in the same place and share the same frequency. — location: [506]() ^ref-40129

---
SSVEP paradigm, several items will be presented on a screen at the same time while the items are shown at variant positions with different frequencies. — location: [507]() ^ref-22576

---
In the VEP paradigm, different visual patterns will be presented on the screen in turn to check the changes in the brain signals of the user. — location: [505]() ^ref-46973

---
The compressed signals were sent through a DBN-RBM algorithm to capture the more abstract high-level features. Maddula — location: [1027]() ^ref-29492

---
The model included a 2D CNN structure to capture the spatial features followed by an LSTM layer for temporal feature extraction. — location: [1029]() ^ref-25534

---
A new model was presented based on CNN, which included five low-level CNN classifiers with the different feature set, and the final high-level results are voted by the low-level classifiers — location: [1035]() ^ref-56994

---
Most of the deep learning-based studies in the SSEP area focus on SSVEP. SSVEP refers to brain oscillations evoked by flickering visual stimuli, which are generally produced in the parietal and occipital regions — location: [1067]() ^ref-22451

---
They used a hybrid method of combined CNN and RNN to capture the meaningful features directly from the time domain, — location: [1069]() ^ref-57460

---
applied a compact CNN model to work directly on the raw SSVEP signals without any handcrafted features. The reported cross-subject mean accuracy was approximately 80%. — location: [1070]() ^ref-26128

---
The proposed model employed a softmax layer for the final classification and achieved an accuracy of 97.78%. — location: [1075]() ^ref-15068

---
Next, we attempt to provide some guidelines for the design of deep learning-based BCI systems derived from our analysis of the state-of-the-art studies. — location: [1147]() ^ref-2633

---
Among the 238 publications surveyed, only seven focused on invasive brain signal research, — location: [1163]() ^ref-5970

---
Furthermore, there are few public data sets of invasive brain signals; invasive data is therefore simply inaccessible to most. — location: [1166]() ^ref-544

---
In terms of the classification of invasive signals, CNN-related algorithms often display a higher capability of recognizing the pulse within cortex neurons. — location: [1167]() ^ref-27622

---
Among those, about 70% of the EEG papers consider spontaneous EEG (133 publications). — location: [1169]() ^ref-26337

---
In terms of the research on MI EEG (30 publications), independent CNN and CNN-based hybrid models were widely used. — location: [1173]() ^ref-64816

---
As for the representative models, DBN-RBM was often applied to capture the latent features from the MI EEG signals. — location: [1174]() ^ref-54633

---
Over half employed representative models (such as D-AE, D-RBM, and especially DBN-RBM) for unsupervised feature learning. — location: [1175]() ^ref-14190

---
Several publications have implemented GAN-based data augmentation. — location: [1181]() ^ref-59462

---
evoked potentials also drew much attention. On the one hand, in ERP, studies using VEP and its subcategory RSVP are common because — location: [1184]() ^ref-65045

---
On the one hand, in ERP, studies using VEP and its subcategory RSVP are common because visual stimuli, compared to other stimuli, are more easily conducted have more real-world applications (e.g., the P300 speller can be used for brain typing). — location: [1184]() ^ref-10524

---
only SSVEP has been studied using deep learning models. — location: [1188]() ^ref-55189

---
Our analysis shows that discriminative models appeared most frequently in the summarized publications — location: [1198]() ^ref-42591

---
Another observation is that CNN represents more than 70% of the discriminative models, for which we provide reasons as follow. — location: [1199]() ^ref-396

---
First, the design of CNN is powerful enough to extract the latent discriminative features and spatial dependencies from the EEG signals for classification. — location: [1200]() ^ref-3124

---
As a result, CNN structures are adopted for classification in some studies and for feature engineering in others. Second, — location: [1201]() ^ref-48122

---
CNN has achieved great success in some research areas (e.g., computer vision), which has made it both extremely well known and feasible (public codes). — location: [1202]() ^ref-38972

---
Third, some brain diagrams (e.g., fMRI) naturally form 2D images conducive to processing by CNN, while other 1D signals (e.g., EEG) are easily converted into 2D images for further analysis by CNN. — location: [1204]() ^ref-52834

---
(1) convert each time point1 to a 2D image; (2) convert a segment into a 2D matrix. — location: [1206]() ^ref-9373

---
For example, single-channel EEG signals can be processed by 1D CNN. — location: [1211]() ^ref-12030

---
In terms of RNN, it was adopted in only about 20% of the discriminative model-based papers, which is far fewer than we had expected since RNN has proved to be powerful at temporal feature learning. — location: [1212]() ^ref-33333

---
MLP is not popular due to its inferior effectiveness (e.g., nonlinear ability) compared to the other algorithms. — location: [1216]() ^ref-32045

---
Among representative models, DBN, especially DBN-RBM, is the most popular model for feature extraction. — location: [1217]() ^ref-10344

---
It can be inferred that researchers preferred to use DBN for feature learning followed by a nondeep learning classifier before 2016; but recently, an increasing number of studies have begun to adopt CNN or hybrid models for both feature learning and classification. — location: [1220]() ^ref-44642

---
Another type of hybrid models is the combination of representative and discriminative models. — location: [1227]() ^ref-11879

---
Different subjects may produce different brain signal patterns, — location: [1416]() ^ref-48681

---
this is known as “intersubject variability” (Saha and Baumert, 2019) and is caused by a number of person-specific factors (such as age, gender, and fatigue) whose fundamental relevances are not yet fully understood (Kanoga et al., 2020). — location: [1416]() ^ref-39943

---
Subject-Dependent. The training and the testing sets are collected from the same subject. — location: [1421]() ^ref-58897

---
Subject. The training set and testing set are acquired from the same group of subjects. — location: [1423]() ^ref-38168

---
Subject-Independent. The training set is gathered from a number of subjects, whereas the testing set is collected from an unseen person who was not part of the training set. — location: [1425]() ^ref-6365

---
As a result, the BCI system can serve any subject from this group but its performance may drop dramatically when applied to individuals beyond the group. — location: [1424]() ^ref-4833

---
As a result, researchers must add constraints and study within narrow parameters (e.g., subject-dependent and cross-subject) in order to shed light on subject-independent developments. — location: [1430]() ^ref-24706

---
the pattern-related component (e.g., the action/status of the subject), — location: [1433]() ^ref-58786

---
the component evoked by objective factors (e.g., environmental noise), — location: [1433]() ^ref-65188

---
and the component evoked by subjective factors (e.g., gender, height, age, health). — location: [1434]() ^ref-55595

---
RNN and its variants are able to extract temporal features; CNN and its variants can explore the latent spatial features; — location: [1441]() ^ref-54810

---
and graph neural networks (GNNs) discover the graphical features based on the connections among brain regions. — location: [1442]() ^ref-49670

---
The independent use of GNNs and the integration of GNNs with other deep learning models present a bright prospect for future research. — location: [1449]() ^ref-28955

---
Apart from the basic models discussed above, the representative deep learning models (e.g., AE and RBM) can perform noise and dimensionality for any feature set, while the MLP structures can be used to learn representations and make predictions in any context. — location: [1455]() ^ref-52898

---
are long and continuous and cannot be directly fed into the downstream stages. — location: [1459]() ^ref-10255

---
Therefore, we slice these long recordings into short segments, each of which is called a sample. This — location: [1460]() ^ref-58360

---
operation is called segmentation. — location: [1461]() ^ref-1210

---
time window and the overlap. The time window is the length of the segment, while the overlap indicates the interval during which two adjacent segments coincide. — location: [1464]() ^ref-16968

---
That means the equipment will take 100 samples per second and that each sampling will produce 64 values (one value per electrode). — location: [1469]() ^ref-43170

---
Taking this one step further, we can regard the horizontal (rows) as the temporal axis and the vertical (columns) as the spatial axis. — location: [1472]() ^ref-47022

---
Es is the noise caused by intersubject variability. — location: [1438]() ^ref-58678

---
Eo is the noise caused by intrasubject variability, and — location: [1437]() ^ref-27264

---
Ep is the signal of interest in BCI system — location: [1437]() ^ref-33132

---
Most of the existing BCI-related studies focus on subject-dependent scenarios, — location: [1474]() ^ref-45186

---
Es approximates to zero, as all the signals are gathered from the same subject. — location: [1477]() ^ref-19956

---
Straightforwardly put, RNN, along with its variants, provides the opportunity to explore temporal representations that indicate how the brain signal varies over time. — location: [1482]() ^ref-43603

---
Then the raw EEG signals are fed into the segmentation stage by setting the time window as 5 s, with an overlap of 0. — location: [1490]() ^ref-29353

---
The time window and overlap are empirically determined, depending on the experimental scenario, signal quality, and even equipment sampling frequency. — location: [1490]() ^ref-43405

---
30 s is set for sleep EEG, 0.1–3 s for MI EEG, and 2–10 s for emotional and mental disease EEG. — location: [1492]() ^ref-31279

---
Next, the segments are fed into the third stage, which is feature engineering. — location: [1494]() ^ref-7807

---
including the cross-correlation feature, time domain features, frequency domain features, and graph-theoretic measures. The cross-correlation feature measures the correlations among each pair of EEG channels to quantify the similarity between any two EEG signals, — location: [1495]() ^ref-29469

---
In the time domain, the commonly used features in brain signal analysis include several statistical moments (mean value, variance, skewness, kurtosis), — location: [1497]() ^ref-26916

---
In addition, the spectral information of the EEG signals is also taken into consideration, since various frequency domain features are also extracted, — location: [1500]() ^ref-32053

---
including the total energy spectrum and the energy percentage across the fundamental rhythmic bands (e.g., Delta, Theta, Alpha, Beta, and Gamma bands). — location: [1501]() ^ref-4703

---
this framework also considers the graph-theoretic measures, which reflect the functional connectivity between the EEG channels — location: [1502]() ^ref-16922

---
The classiﬁer is comprised of six layers: the ﬁrst LSTM layer contains 643 cells, where each cell receives one feature extracted in the previous stage. Next, a dropout layer with a dropout rate of 0.5 is adopted to prevent overﬁtting. — location: [1506]() ^ref-47167

---
layer randomly sets 50% of the cell outputs as zero to force the LSTM to learn more generalized representations. — location: [1508]() ^ref-48220

---
The third layer is another LSTM layer containing 128 cells, followed by a dropout layer with a 0.2 dropout rate. — location: [1508]() ^ref-57605

---
Note that, the manual feature extraction in the third stage is essential in traditional BCI systems but can be omitted in deep learning-based BCIs because deep learning can automatically learn features from raw — location: [1512]() ^ref-24348

---
EEG signals. — location: [1513]() ^ref-14708

---
On the ﬁrst occasion, the LSTM classiﬁer receives raw EEG signals and directly identiﬁes the epileptic seizure stage without feature learning. On the second occasion, the LSTM classiﬁer takes the manually extracted feature as its basis for prediction. The experimental results show that the second classiﬁer outperforms the ﬁrst with a margin of around 10%. — location: [1514]() ^ref-38186

---
This indicates that combining of traditional features with state-of-the-art deep learning models is a good way to boost the performance of BCI systems. — location: [1516]() ^ref-55338

---
Let us continue take epileptic seizure detection as the application scenario, CNN has been adopted to capture spatial features from both the time-domain and frequency-domain of EEG signals. — location: [1522]() ^ref-6250

---
The frequency domain segments are transformed from the time domain through fast Fourier transform (FFT). — location: [1527]() ^ref-10263

---
Convolutional networks may include local or global pooling layers that combine the outputs of neuron clusters from one layer into a single neuron in the next layer. — location: [1535]() ^ref-30420

---
Compared to a conventional CNN, the highlight of this framework is its two branches of input. Speciﬁcally, not only the usual spatial information in time domain is considered; representations in the frequency domain are also captured. — location: [1544]() ^ref-31491

---
time/frequency dimension, a channel dimension, and a sample dimension, — location: [1528]() ^ref-5103

---
whereas in fact, they prove to contain only two dimensions if we take a closer look at a single sample. — location: [1529]() ^ref-47989

---
In early integration, information is combined in the input layer. For example, we have a sample with shape [100, 64] in the time domain and, by performing FFT, obtain a shape [100, 64] — location: [1549]() ^ref-18611

---
Next,they are fused into a matrix with shape [100, 128] and then use CNN is used to analyze the newly formed matrix. — location: [1551]() ^ref-51147

---
The middle integration method, as illustrated in Figure 6.2, combines features in hidden layers. — location: [1552]() ^ref-50704

---
In the late integration method, analysis is independently performed on each input data and the model results are combined to make the ﬁnal prediction. For example, we could build two identical CNN classiﬁers, where one receives time domain samples and the other receives frequency domain samples, and then, the average of the output layer of the two — location: [1552]() ^ref-25639

---
classiﬁers is taken as the ﬁnal predicted output. EEGNET (Lawhern et al., 2018) is a popular network that can explicitly learn spatial relationships from raw EEG signals. — location: [1555]() ^ref-9504

---
model contains several branches to learn different aspects of the input EEG signals in parallel and at last combine the learned representation for ﬁnal classiﬁcation. — location: [1556]() ^ref-35489

---
Deep learning models generally treat the EEG channels as a 2D grid input, neglecting the complex connections among the EEG channels (Li et al., 2019). — location: [1562]() ^ref-28161

---
The graphical representation analysis is based on graph theory, according to which each brain region (e.g., EEG electrode) is represented as a vertex, while the connection among regions is represented by an edge. — location: [1563]() ^ref-39016

---
the graphical connection among ﬁve channels in the frontal (F) and temporal (T) lobes of the human brain. The exact connections among brain regions are still not deﬁnitely understood by biological and neurological researchers; — location: [1566]() ^ref-24319

---
GNNs have drawn much attention in the past two years, and there are already numerous variants; please refer to Wu et al. (2020) — location: [1581]() ^ref-10028

---
Compared to a standard CNN, the key modiﬁcation of a GCN is a novel developed convolutional operation called the graph convolutional operation. Rather — location: [1583]() ^ref-31936

---
First, the “information” in each channel is calculated through a nonlinear transformation. — location: [1585]() ^ref-48441

---
is sampled at F7 channel at a time point. The hF7 denotes the “information”carried by channel F7 — location: [1589]() ^ref-36534

---
Since this is a fully connected graph, the neighboring nodes contain AF3, F3, FC5, and T7. The aggregated information  is calculated — location: [1591]() ^ref-10949

---
wAF3 represents the importance weights (or edge weight) of channels AF3 to F7. The weight is calculated as — location: [1594]() ^ref-28691

---
DAF3 denotes the “degree” of vertex AF3 meaning the amount of AF3’s neighbors — location: [1596]() ^ref-46265

---
Here, the adjacency matrix is built based on predeﬁned brain connectivity, as shown in Figure 6.5 — location: [1601]() ^ref-33491

---
propose a GNN-based framework for mapping regional and cross-regional functional activation patterns for classiﬁcation tasks, such as distinguishing patients with neurological disorders from healthy control subjects and performing cognitive task decoding. — location: [1610]() ^ref-21872

---
The BrainGNN is a GNN variant modiﬁed to aggregate node information only from selected neighbors rather than the entire neighborhood. — location: [1615]() ^ref-5531

---
To prevent conflict between temporal and spatial features within a single EEG sample, researchers have developed an effective method for converting 1D EEG time points to a 2D matrix. — location: [1623]() ^ref-8776

---
The gray circle on the right side is set as 0, whereas the brown circles inherit the values of collected elements. — location: [1625]() ^ref-61272

---
We here introduce two typical frameworks combining RNN and CNNs in cascade and parallel, respectively. The former learns temporal and spatial representations sequentially, while the latter learns temporal and spatial representations in parallel and combines them for prediction. — location: [1631]() ^ref-62013

---
the data input, spatial representation learning, temporal representation learning, and calculation of the prediction results. — location: [1633]() ^ref-62367

---
CNN structure is adopted to learn the latent spatial correlations from each EEG sample. In this example, 10 2D CNNs are adopted, and each CNN receives one time point and extracts a spatial feature vector. — location: [1637]() ^ref-65284

---
In the stage which follows, the learned spatial representations are fed into a temporal feature extractor composed of two LSTM layers. — location: [1639]() ^ref-15432

---
contrast to the cascade model, this framework extracts the spatial and temporal representations simultaneously and performs a middle-integration to fuse features in order to make the ﬁnal prediction. — location: [1646]() ^ref-25360

---
We have ourselves made a preliminary exploration of these topics. In this book, we propose a BCI system which captures spatial graphical representations to print a replica of an imagined object — location: [1653]() ^ref-47896

---
However, recalling Equation (6.1), under the cross-subject situation, the model must also handle the Es caused by inter-subject variability. — location: [1659]() ^ref-55334

---
but they would not perform well due to intersubject variability. — location: [1661]() ^ref-34665

---
The ﬁrst is fairly straightforward: enhancing the data size so as to force the machine learning model to learn the latent patterns. — location: [1662]() ^ref-22333

---
This strategy is not only costly in terms of data, as it requires massive brain signal samples, it cannot even theoretically guarantee a good prediction accuracy. — location: [1663]() ^ref-6252

---
The second strategy is to design a deep learning framework capable of extracting puriﬁed representations (from which the noise caused by intersubject variability has been removed). — location: [1664]() ^ref-62523

---
First we analyze the similarity of EEG signals and calculates the correlation coefficients matrix for both interclass and cross-subject conditions. — location: [1668]() ^ref-15322

---
Next, we extract EEG signal features by applying the autoencoder algorithm — location: [1669]() ^ref-19724

---
The features are then fed into a XGBoost classiﬁer which identiﬁes the EEG data categories, where each category corresponds to a speciﬁc intent. — location: [1669]() ^ref-3192

---
Both self-similarity and cross-similarity are measured under two conditions: interclass and cross-subject. — location: [1679]() ^ref-12670

---
Interclass Measurement. Under the interclass situation, we measure the correlation coefficient matrix for each specific subject and calculate the average matrix by calculating the mean value of the entire matrix. — location: [1680]() ^ref-50372

---
In this matrix,  denotes the correlation coefficient between the samples from the class  and the samples from the class — location: [1683]() ^ref-55790

---
similarity between two different samples from the same class. — location: [1684]() ^ref-58413

---
Cross-similarity indicates the average similarity of each possible class pair of samples belonging to one specific subject. — location: [1685]() ^ref-9076

---
Subject Measurement. Under the cross-subject situation, we measure the correlation coefficients matrix for each specific class and then calculate the average matrix. — location: [1686]() ^ref-60975

---
Cross — location: [1686]() ^ref-25388

---
-similarity indicates the average similarity of each possible subject pair of samples belonging to the specific class. — location: [1688]() ^ref-58183

---
measurement: self-similarity and cross-similarity. Self- — location: [1678]() ^ref-28521

---
Self-similarity is defined by the similarity of EEG signals within the same EEG category, whereas cross-similarity is deﬁned as the similarity of EEG signals from two different EEG categories — location: [1678]() ^ref-58389

---
We can observe from the results that the self-similarity is always higher than the cross-similarity for all classes, meaning that the samples’ intraclass cohesion is stronger than their interclass cohesion. — location: [1691]() ^ref-27444

---
an alternative visualization of the results. — location: [1697]() ^ref-17927

---
Again, we ﬁnd that, for each class, the self-similarity is higher than cross-similarity, with varying percentage differences. The standard deviations of cross-similarity — location: [1698]() ^ref-40373

---
(1) Self-similarity is consistently higher than cross-similarity under both interclass and cross-subject conditions; (2) the higher the interclass percentage difference, the better the classiﬁcation results; and (3) lower average percentage differences and standard deviations of the subjects result in better classiﬁcation performance under the cross-subject condition. — location: [1700]() ^ref-62669

---
Normalization plays a crucial role in a knowledge discovery process when dealing with parameters of different units and scales. — location: [1708]() ^ref-45557

---
For instance, assuming that one input feature ranges from 0 to 1, whereas another ranges from 0 to 100, without adjustment, the analysis results would be dominated by the latter feature. — location: [1709]() ^ref-53352

---
The experimental results — for complete details refer to Zhang et al. (2017c) — show — location: [1731]() ^ref-24277

---
that the z-score scaling normalization obtains the best classiﬁcation performance, whereas the unity normalization obtains the worst. — location: [1732]() ^ref-65173

---
In our prior experience, a basic autoencoder works better than a stacked autoencoder when dealing with EEG signals; — location: [1742]() ^ref-29394

---
represents the learned feature in the hidden layer for the ith sample, where M denotes the number of neural units in the current layer (the number of elements in hi). For simplicity’s sake, we use x and h to represent the input data and the data in the hidden layer, respectively. — location: [1745]() ^ref-42298

---
The discrepancy between x and x′ is calculated by the MSE (mean squared error) cost function which is optimized by the RMSPropOptimizer. — location: [1753]() ^ref-4686

---
In summary, the process of training an autoencoder is the task of optimizing the parameters to achieve the minimum cost between the input x and the reconstructed data x′. — location: [1754]() ^ref-35036

---
The autoencoder entails either dimensionality reduction if d > M or dimensionality increase if d < — location: [1758]() ^ref-45414

---
XGBoost, or Extreme Gradient Boosting, is a supervised scalable tree boosting algorithm derived from the concept of the gradient boosting machine (Friedman, 2001). — location: [1761]() ^ref-26263

---
The XGBoost model is an ensemble of a set of classiﬁcation and regression trees (CART), each having its leaves and corresponding scores. The ﬁnal results of such a tree ensemble is the sum of all its individual trees. — location: [1766]() ^ref-25233

---
The regularization function is the most outstanding contribution of XGBoost. It calculates the complexity of the model and applies a larger penalty to a more complex structure. — location: [1773]() ^ref-64144

---
The regularized objective function helps to deliver both a simple structure model and predictive functions. — location: [1779]() ^ref-63957

---
Transfer learning is a subdomain of machine learning that takes knowledge learned from one task (i.e., the source task) and reuses it in performing another similar task (i.e., the target task) (West et al., 2007). — location: [1788]() ^ref-63978

---
variety of subjects and then tune the model to work on an unseen subject. — location: [1799]() ^ref-55780

---
Here, we introduce a representative transfer learning framework proposed in Tu and Sun (2012). In this approach a new model is trained on the data from a pool of subjects and then transfers the learned knowledge to a new subject. — location: [1804]() ^ref-6614

---
To begin with, a candidate filter bank is built based on the Extreme Energy Ratio (EER) criterion (Sun, 2008). The — location: [1807]() ^ref-64155

---
EER learns spatial filtering that maximizes the variance of spatially filtered EEG samples belonging to one class while minimizing the variance of other classes. — location: [1808]() ^ref-1951

---
the robust filter bank and the adaptive filter. — location: [1810]() ^ref-46697

---
Some signals are not sensitive to subject, that is, the signals don’t contain — location: [1812]() ^ref-37164

---
Es — location: [1813]() ^ref-16088

---
To this end, for K source subjects, we have K robust classifier and K adaptive classifier. — location: [1818]() ^ref-44990

---
(Refer to Tu and Sun (2012) for further details on how to select for the robust and adaptive filter banks.) — location: [1814]() ^ref-28539

---
a dynamic ensemble strategy is employed to combine the outcomes of the K classifiers. — location: [1819]() ^ref-50869

---
A learned parameter is used to trade off the robustness and adaptiveness in the final prediction. — location: [1822]() ^ref-58896

---
For example, a classification model can attain great performance in neurological disorder diagnosis but fail at emotion recognition. — location: [1828]() ^ref-63940

---
