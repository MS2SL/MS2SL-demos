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
**Text:**

<table style="width: 100%; margin-left: auto; margin-right: auto;">
    <tr>
    	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Raw video </td>
    	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; GT </td>
	<td> &nbsp;&nbsp;&nbsp; Ham2Pose </td>
	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; T2M-GPT </td>
	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Ours </td>
    </tr>
    <tr>
    	<td><audio src="./samples/ss_reverb/source_1221-135766-0003_0.0018.wav" controls style="width: 150px;"></audio> </td>
    	<td><audio src="./samples/ss_reverb/gt_1221-135766-0003_0.0018.wav" controls style="width: 150px;"></audio> </td>
    	<td><audio src="./samples/ss_reverb/image2reverb/metric_source_1221-135766-0003_0.0018.wav" controls style="width: 150px;"></audio> </td>
	<td><audio src="./samples/ss_reverb/avatir/vida_source_1221-135766-0003_0.0018.wav" controls style="width: 150px;"></audio> </td>
	<td><audio src="./samples/ss_reverb/1221-135766-0003_0.0018.wav" controls style="width: 150px;"></audio> </td>
    </tr>
</table>

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Text:**

<table style="width: 100%; margin-left: auto; margin-right: auto;">
    <tr>
    	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Raw video </td>
    	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; GT </td>
	<td> &nbsp;&nbsp;&nbsp; Ham2Pose </td>
	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; T2M-GPT </td>
	<td> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Ours </td>
    </tr>
    <tr>
    	<td><audio src="./samples/ss_reverb/source_1221-135766-0003_0.0018.wav" controls style="width: 150px;"></audio> </td>
    	<td><audio src="./samples/ss_reverb/gt_1221-135766-0003_0.0018.wav" controls style="width: 150px;"></audio> </td>
    	<td><audio src="./samples/ss_reverb/image2reverb/metric_source_1221-135766-0003_0.0018.wav" controls style="width: 150px;"></audio> </td>
	<td><audio src="./samples/ss_reverb/avatir/vida_source_1221-135766-0003_0.0018.wav" controls style="width: 150px;"></audio> </td>
	<td><audio src="./samples/ss_reverb/1221-135766-0003_0.0018.wav" controls style="width: 150px;"></audio> </td>
    </tr>
</table>


## Audio-to-Sign
