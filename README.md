# prestack {#prestack}

*

![http://sharpreflections.com/wp-content/uploads/2016/03/prestackPro-fullcolor.png](C:\Temp\Gitbook3\export\assets\httpsharpreflectionscomwp-cont.png)

USER MANUAL

FOR

Pre-Stack Pro version 4.10

Stavanger London Kaislerslautern, 2017

Introduction 11

1 Getting started 12

1.1 Checking and change status of parallel file system 12

1.2 Start of Pre-Stack Pro 12

1.3 Appearance 13

1.3.1 Data Pool 14

1.3.2 Workflow 17

1.3.3 Processing tab 17

1.3.4 Viewer windows 17

1.3.5 Windows hide/show 18

2 Create a new Project 18

3 Restore a project 22

4 Unit Support 23

5 Open and edit an existing project 25

5.1 Open project 25

5.2 Edit project geometry 26

6 Import data 26

6.1 Import SEG-Y 27

6.1.1 Loading regular data 33

6.1.2 Loading &#039;irregular&#039; data 37

6.1.2.1 Set regularization parameters 39

6.1.3 Import 2D SEG-Y 41

6.1.4 Import Arbitrary Path 41

6.1.5 Import of multi-azimuth SEG-Y 41

6.1.6 Import JavaSeis 45

6.1.6.1 The axis definition tab 46

6.1.6.2 Volume properties tab 47

6.1.6.3 Axes scaling 47

6.1.6.4 Volume dimensions 48

6.2 Common ASCII import features 49

6.2.1 File Selection 49

6.2.2 Format definition 49

6.2.3 Object name 50

6.2.4 Picking the live data 50

6.2.5 Additional parameters tab 51

6.2.6 User Comments tab 52

6.2.7 Import, Import All and Apply 52

6.3 Import Horizon 52

6.4 Importing Well Data 53

6.4.1 Import Well Heads 53

6.4.2 Import Well Path 55

6.4.3 Import T/D table or Checkshots 57

6.4.4 Import Well Tops 59

6.4.5 Import Well logs from LAS files 61

6.5 Import Polygons 62

6.6 Import Velocity 65

6.6.1 ASCII 65

6.6.1.1 3D ASCII 65

6.6.1.2 2D ASCII 68

6.6.2 SEGY 69

6.6.2.1 3D SEGY 69

6.6.2.2 2D SEGY 69

6.7 Import Q data 70

6.8 Import ETA field 70

6.9 Import Wavelets from ASCII 71

6.10 Import Cultural Data 72

7 Select Data 73

7.1 Interactive data selection 74

7.2 Select velocity 78

7.3 Select Q data, SRMS data or ETA 80

8 Save Data into Project 81

9 File Manager 82

9.1 Delete data 83

9.2 Edit data 84

9.2.1 Rename 84

9.2.2 Edit option 84

9.3 Select from file 86

9.4 Shared Projects 87

9.4.1 Create a shared project 87

9.4.2 Open shared project and transfer data 87

9.4.3 Close shared project 88

9.5 Select from file 88

10 Data export 88

10.1 SEG-Y Export 89

10.1.1 Trace header interpolation 93

10.2 ASCII Export of map 94

11 Session management 95

11.1 Saving a session 95

11.2 Restoring a session 95

12 Viewers 96

12.1 Functionalities common to all viewers 96

12.1.1 Visualization of datasets 96

12.1.2 Histograms 100

12.1.3 Overlays 104

12.1.4 Synchronization 105

12.2 3D Viewers 107

12.2.1 Load and display data 108

12.2.2 Histogram (Color bar) and Transfer Function 110

12.2.3 Edit display 111

12.2.4 Camera positions 113

12.2.5 Horizons 114

12.3 Spectral Analysis 114

12.4 2D Data Comparator 117

12.4.1 Data selection 119

12.4.2 Comparing data 120

_12.4.3_ Attributes extraction 122

12.4.4 Calculate Attributes 126

12.5 Single Trace Viewer 129

12.6 2D Map Viewer 129

12.6.1 Map viewer tool bar 132

12.6.2 Zoom 133

12.6.3 Arbitrary lines 133

12.6.4 Polygons 135

12.6.5 Locations of Interest 136

12.6.6 Display 2D Lines 136

12.7 2D Gather Viewer 137

12.7.1 Horizons 137

12.7.2 Wells 137

12.7.3 Arbitrary lines 137

12.7.4 Display data as Wiggle plot 138

12.7.5 Displaying gathers from 2D lines 139

12.8 Stack Viewer 139

12.8.1 Seismic section polygons 140

12.8.2 Displaying stacks from 2D lines 141

12.9 2D Top Stack Viewer 141

12.10 2D PreStack Map Viewer 143

12.11 Cross Plot 144

12.12 Well log viewer 163

12.12.1 Introduction 163

12.12.2 Log data Q.C. &amp; management 165

12.12.2.1 Linked log viewer 169

12.12.3 Well Log Viewer GUI 169

12.12.4 Well Log Viewer icons 174

13 Algorithm documentation 175

13.1 Overview of the process window 176

13.1.1 Overview 176

13.1.2 Functionalities 180

13.1.3 Edit Mode 180

13.1.4 Copy 181

13.2 Attributes 181

13.2.1 Volume Calculator 181

13.2.1.1 Subtraction, summation, multiplication, division 182

13.2.1.2 Add Noise 183

13.2.1.3 Limit Amplitude 184

13.2.1.4 Custom equation 185

13.2.2 Spectral Attribute Calculator 187

13.2.3 AVA Attribute Calculator 188

13.2.4 Complex Trace Attribute Calculator 191

13.2.5 Moving Window Statistics 192

13.2.6 Normalized RMS 194

13.2.7 Auto/Cross-correlation 194

13.2.8 Structural Dip 195

13.2.9 Dip-steered Semblance 196

13.2.10 Semblance Multi-input 197

13.2.11 Extrema 197

13.2.12 Signal to Noise Ratio 198

13.2.13 Geometric Properties 200

13.2.14 Gather attributes 201

13.3 Processing 205

13.3.1 NMO 205

13.3.2 Stack|Mute 208

13.3.2.1 Use mutes 209

13.3.2.2 Project Mute 210

13.3.3 Partial Stacking 211

13.3.4 Butterworth Filter 213

13.3.5 Frequency Filter 214

13.3.6 User Defined Filter 216

13.3.7 Spatial Smoothing Filter 218

13.3.8 Destriping 219

13.3.9 Median Filter 220

13.3.10 ECED 2D and 3D 221

13.3.11 EPS 3D 223

13.3.12 Gaining 226

13.3.13 Attenuation 229

13.3.13.1 Q-Filter 230

13.3.13.2 Q model 230

13.3.14 Radon 231

13.3.15 Inverse Radon 236

13.3.16 Tau-P Deconvolution 239

13.3.17 Dip Filter 242

13.3.18 Adaptive Subtraction 244

13.3.19 RMO 245

13.3.20 RMO (Time Shift) 247

13.3.21 Semblance Optimization 248

13.3.22 Align 2 253

13.3.23 Continuous Velocity Analysis 258

13.3.24 Velocity Editor 259

13.3.24.1 Create Velocity Functions 259

13.3.24.2 Main window 261

13.3.24.3 Parameters 262

13.3.24.4 Edit velocity functions 263

13.3.24.5 Link to a map 264

13.3.25 Phase rotation 265

13.3.26 Spectral Balance 266

13.3.27 Bandwidth Extension 269

13.3.28 Fast Fourier Transformation 270

13.3.29 Inverse Fast Fourier Transformation 271

13.3.30 Time Depth Conversion, Seismic and Horizon 272

13.3.31 Seismic RMS amplitude calculation 274

13.3.32 Velocity Conversion 274

13.3.33 Trace Interpolation 275

13.3.34 Offset Trace Interpolation 277

13.3.35 Bulk Time Shift 278

13.3.36 COCA Sectorization 278

13.4 Interpretation-Processing 279

13.4.1 Offset to Angle 279

13.4.2 Angle to offset 283

13.4.3 PCube Background Model Builder 283

13.4.4 Feasibility Modelling 288

13.4.5 3D Parametric Synthetic Model Builder 293

13.4.6 Generate Synthetic Gather 310

13.4.7 PCube Inversion 318

13.4.8 Pcube+ 323

13.4.8.1 Introduction 323

13.4.8.2 Input Setup 324

13.4.8.3 Background Model 326

13.4.8.4 Transition Probabilities 329

13.4.8.5 Parameter Tuning 332

13.4.8.6 Output Setup 335

13.4.8.7 Results 335

13.4.8.8 Pcube+ Inspector 338

13.4.9 Shuey Modelled gather 339

13.4.10 Chi Angle 339

13.4.11 Trace Integration 340

13.4.12 AVO Scaling 340

13.4.13 Multi-Well Scalar 342

13.4.14 Sculpt 343

13.4.15 Volume flattening and unflattening 345

13.4.15.1 Volume flattening 346

13.4.15.2 Volume unflattening 347

13.4.16 Horizon Toolkit 348

13.4.16.1 AutoTrack in Stack 349

13.4.16.2 Despike and Gridding 355

13.4.16.3 Extend Horizon to Pre-Stack 356

13.4.16.4 Horizon Calculator 358

13.4.16.5 Time / Depth Conversion 359

13.4.17 Wavelet tool 360

13.4.17.1 Introduction and working with the tool 360

13.4.17.2 Wavelet Management and Display 363

13.4.17.3 Example Workflows 375

13.4.17.4 Description of Functions 388

13.4.18 Create Maps 389

13.4.18.1 The parameters 390

13.4.18.2 Users tips 394

13.4.19 Create interval maps 395

13.4.19.1 The parameters 396

14 Workflow 399

14.1 Overview 401

14.2 Creation and editing of a workflow 405

14.2.1 Create a workflow from volume 405

14.2.2 Editing of a workflow 407

14.2.2.1 Saving a volume 407

14.2.2.2 Make a workflow editable 408

14.2.2.3 Algorithm Parameters editing 410

14.2.2.4 Sequence editing 410

14.2.3 Save a workflow 417

14.3 Execute and Queue workflows 418

14.3.1 Loading a workflow 418

14.3.2 Input a volume from the Data Pool in a workflow 421

14.3.3 Load invalid workflow 421

14.3.4 Load a workflow with Preview 426

14.3.5 Execution 427

14.3.6 Queue 429

14.4 Workflows for multiple files 431

14.4.1 Adding output files from workflows to File Groups 434

15 Utilities and Setting 435

15.1 Create Pseudo Pre-Stack 435

15.2 Merge Volumes 436

15.3 Manage Facies 438

15.4 Manage Wavelets 439

15.5 View/Compare Probabilities 440

15.6 Combine Volumes 441

15.7 Coordinate Converter 443

15.8 Units Converter 444

15.9 Create Window Screenshots 444

16 Settings 445

17 Help 447

18 Pre-Stack Pro Installation and troubleshooting 448

18.1 Requirements 448

18.1.1 Minimum system requirements for Pre-Stack Pro 449

18.1.2 Known Working systems 450

18.2 Installation step by step 451

18.2.1 Configure network connection 451

18.2.2 Make the infiniband connection work 452

18.2.3 Test the Infiniband connection 454

18.2.3.1 Performance recommendation. 455

18.2.3.2 Installation of Nvidia drivers, only needed on remote viewer machine. 455

18.2.4 Installation of the BeeGFS Parallel File System 455

18.2.5 Installation of Pre-Stack Pro on two or more nodes 456

18.2.6 Installation on a cluster 456

18.2.7 Configuration for GPI2 457

18.2.7.1 Memlock 457

18.2.7.2 SSH 458

18.2.7.3 Machinefile 458

18.2.8 Installation of OLicense Server 459

18.2.8.1 Server installation 459

18.2.8.2 Requesting your license file 460

18.2.8.3 Installing the license file 460

18.2.8.4 Directing Pre-Stack Pro to your license server 461

18.2.9 Pre-Stack Pro User accounts 461

18.2.10 PreStackProBackendrc configuration file 462

18.2.11 Upgrading Pre-Stack Pro 463

18.3 Getting started 464

18.3.1 Starting Pre-Stack Pro 464

18.3.1.1 Starting the client 464

18.3.1.2 Start of the backend server 464

18.4 Troubleshooting/FAQ 466

18.4.1 How to check the status of the parallel file system 466

18.4.2 Frequently Asked Questions 466

18.5 Support 467

19 Appendix 469

19.1 Project upgrade to 4.0 469

19.2 ECED 469

19.2.1 Mathematical background 469

19.2.2 Numerical scheme 470

19.3 Open Source Licenses 471

19.3.1 BSD License 471

19.3.2 LGP License 472

19.3.3 CP License 484

19.3.4 Apache License 485