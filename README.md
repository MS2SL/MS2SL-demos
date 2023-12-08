# MS2SL: Multimodal Spoken Data-Driven Continuous Sign Language Production
While current sign language translation technology has made significant strides, there is still no viable solution for generating sign sequences directly from spoken content, e.g., text or speech. 
In this paper, we propose a unified framework for continuous sign language production toease communication between sign and non-sign language users. The framework can capably convert multimodal 
spoken data (speech or text) into continuous sign keypoint sequences. In particular, a sequence diffusion model is crafted to step-by-step generate sign predictions, employing text or speech audio 
embeddings extracted by pretrained models like CLIP and HuBert. Moreover, by formulating a joint embedding space for text, audio, and sign, we bind data from the three modalities and leverage the 
semantic consistency across modalities to provide informative feedback signals for the training of diffusion model. This embedding-consistency learning strategy minimizes the reliance on triplet 
sign language data and ensures continuous model refinement, even with a missing audio modality. Experiments on the How2Sign and PHOENIX14T datasets demonstrate that our model achieves competitive 
performance in producing signs from both speech and text data.

# How2Sign
## Text-to-Sign
**Text:** Let me demonstrate you this on my back because it's a lot easier.

<table style="width: 100%; margin-left: auto; margin-right: auto;">
    <tr>
    	<td> &nbsp;&nbsp;&nbsp;Raw video </td>
    	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; GT </td>
	<td> &nbsp;&nbsp;&nbsp; Ham2Pose </td>
	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; T2M-GPT </td>
	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Ours </td>
    </tr>
    <tr>
    	<td><img src="samples/g0iPSnQt6w_14-1-rgb_front/g0iPSnQt6w_14-1-rgb_front.gif" width="114" height="150"></td>
    	<td><img src="samples/g0iPSnQt6w_14-1-rgb_front/gt--g0iPSnQt6w_14-1-rgb_front.gif" width="114" height="150"></td>
    	<td><img src="samples/g0iPSnQt6w_14-1-rgb_front/ham2pose--g0iPSnQt6w_14-1-rgb_front_slow.gif" width="114" height="150"></td>
	<td><img src="samples/g0iPSnQt6w_14-1-rgb_front/t2m-gpt--g0iPSnQt6w_14-1-rgb_front_slow.gif" width="114" height="150"></td>
	<td><img src="samples/g0iPSnQt6w_14-1-rgb_front/ms2sl--g0iPSnQt6w_14-1-rgb_front_slow.gif" width="114" height="150"></td>
    </tr>
</table>

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Text:** I have got some leather mittens here.

<table style="width: 100%; margin-left: auto; margin-right: auto;">
    <tr>
    	<td> &nbsp;&nbsp;&nbsp;Raw video </td>
    	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; GT </td>
	<td> &nbsp;&nbsp;&nbsp; Ham2Pose </td>
	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; T2M-GPT </td>
	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Ours </td>
    </tr>
    <tr>
    	<td><img src="samples/fzOH00UZg84_2-8-rgb_front/fzOH00UZg84_2-8-rgb_front.gif" width="114" height="150"></td>
    	<td><img src="samples/fzOH00UZg84_2-8-rgb_front/gt-fzOH00UZg84_2-8-rgb_front.gif" width="114" height="150"></td>
    	<td><img src="samples/fzOH00UZg84_2-8-rgb_front/ham2pose-fzOH00UZg84_2-8-rgb_front_slow.gif" width="114" height="150"></td>
	<td><img src="samples/fzOH00UZg84_2-8-rgb_front/t2m-gpt-fzOH00UZg84_2-8-rgb_front_slow.gif" width="114" height="150"></td>
	<td><img src="samples/fzOH00UZg84_2-8-rgb_front/ms2sl-fzOH00UZg84_2-8-rgb_front_slow.gif" width="114" height="150"></td>
    </tr>
</table>


## Audio-to-Sign

**Text:**
<audio src="./samples/ss_reverb/1221-135766-0003_0.0018.wav" controls style="width: 150px;"></audio>

<table style="width: 100%; margin-left: auto; margin-right: auto;">
    <tr>
    	<td> &nbsp;&nbsp;&nbsp;Raw video </td>
    	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; GT </td>
	<td> &nbsp;&nbsp;&nbsp; Ham2Pose </td>
	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; T2M-GPT </td>
	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Ours </td>
    </tr>
    <tr>
    	<td><img src="path_to_your_gif.gif" width="114" height="150"></td>
    	<td><img src="path_to_your_gif.gif" width="114" height="150"></td>
    	<td><img src="path_to_your_gif.gif" width="114" height="150"></td>
	<td><img src="path_to_your_gif.gif" width="114" height="150"></td>
	<td><img src="path_to_your_gif.gif" width="114" height="150"></td>
    </tr>
</table>

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Text:**
<audio src="./samples/ss_reverb/1221-135766-0003_0.0018.wav" controls style="width: 150px;"></audio>

<table style="width: 100%; margin-left: auto; margin-right: auto;">
    <tr>
    	<td> &nbsp;&nbsp;&nbsp;Raw video </td>
    	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; GT </td>
	<td> &nbsp;&nbsp;&nbsp; Ham2Pose </td>
	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; T2M-GPT </td>
	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Ours </td>
    </tr>
    <tr>
    	<td><img src="path_to_your_gif.gif" width="114" height="150"></td>
    	<td><img src="path_to_your_gif.gif" width="114" height="150"></td>
    	<td><img src="path_to_your_gif.gif" width="114" height="150"></td>
	<td><img src="path_to_your_gif.gif" width="114" height="150"></td>
	<td><img src="path_to_your_gif.gif" width="114" height="150"></td>
    </tr>
</table>
