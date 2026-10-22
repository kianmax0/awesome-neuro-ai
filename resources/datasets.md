# Datasets and data portals

[Home](../README.md) · [Start here](../start-here/README.md) · [Learn](../learn/README.md) · [Topics](../topics/README.md) · [Resources](README.md) · [Projects](../projects/README.md) · [Community](../community/README.md)

These collections differ in species, measurement, and access. Most contain recorded neural or behavioral measurements; the Spiking Heidelberg Datasets instead provide model-generated spike representations of audio. Use the table to compare candidate sources, then check the details and original source. A data portal helps locate collections with different designs and licenses.

| Resource | Measurement | Useful for | Access |
| --- | --- | --- | --- |
| [Natural Scenes Dataset](#natural-scenes-dataset) | Human 7T fMRI; eight participants viewing natural images | Visual encoding, decoding, and brain–model comparisons | Data access requires an agreement. |
| [Allen Brain Observatory](#allen-brain-observatory) | Mouse visual system; two-photon imaging and Neuropixels | Separate Visual Coding and Visual Behavior collections | Follow the collection access instructions. |
| [THINGS-data](#things-data) | Human fMRI, MEG, and behavioral similarity judgments linked by object stimuli | Encoding and representational similarity analysis (RSA) | Neural data are open; original THINGS images have academic-use restrictions; a separate THINGSplus subset is license-free. |
| [DANDI Archive](#dandi-archive) | Portal for neurophysiology collections, including NWB recordings and FALCON datasets | Search and inspect individual Dandiset metadata to select recordings | Licenses and access state vary by collection; check each Dandiset. |
| [IBL Brainwide Map](#ibl-brainwide-map) | Mouse spike-sorted Neuropixels activity and decision-task variables | Encoding/decoding of stimulus, choice, feedback, and movement across sampled regions | Public through ONE/S3 under CC BY 4.0; use quality filters and current release metadata. Coverage is pooled across sessions and animals. |
| [Narratives](#narratives) | Human fMRI during naturalistic spoken stories | Compare acoustic or language-model features with brain responses | OpenNeuro data declare CC0; story audio has separate noncommercial scholarly reuse conditions. Participants heard different subsets of stories. |
| [Spiking Heidelberg Datasets](#spiking-heidelberg-datasets) | Cochlear-model spike events generated from spoken audio; not biological recordings | Temporal SNN classification with SHD digits and SSC commands | Public HDF5 files under CC BY 4.0; SHD has train/test partitions, SSC also has validation, and SHD's test set includes both held-out and training-set speakers. |

## Dataset details

### Natural Scenes Dataset

- [Natural Scenes Dataset](https://naturalscenesdataset.org/) - Human 7T fMRI recordings from eight participants viewing natural images, supporting visual encoding, decoding, and brain–model comparisons. Data access requires an agreement.

### Allen Brain Observatory

- [Allen Brain Observatory](https://alleninstitute.github.io/brain_observatory_ecosystem/) - Mouse visual-system datasets spanning two-photon imaging and Neuropixels recordings, with separate Visual Coding and Visual Behavior collections.

### THINGS-data

- [THINGS-data](https://vicco-group.github.io/THINGS-data/) - A multimodal collection connecting human fMRI, MEG, and behavioral similarity judgments through shared object stimuli, with derivatives and analysis examples for encoding and RSA. Neural data are openly available; original THINGS stimulus images have academic-use restrictions, with a separate license-free THINGSplus subset.

### DANDI Archive

- [DANDI Archive](https://dandiarchive.org/) - A data portal hosting neurophysiology collections, including NWB recordings and FALCON datasets. Use its search, streaming examples, and individual Dandiset metadata to choose suitable recordings; it is not one uniform dataset, and licenses and access state must be checked per collection.

### IBL Brainwide Map

- [IBL Brainwide Map](https://docs.internationalbrainlab.org/notebooks_external/2025_data_release_brainwidemap.html) - Spike-sorted Neuropixels activity and task variables from mice performing a standardized visual decision task, supporting encoding/decoding and comparisons across sampled brain regions. Data are public through ONE/S3 under CC BY 4.0; brainwide coverage is pooled across sessions and animals, so use quality filters and current release metadata.

### Narratives

- [Narratives](https://snastase.github.io/datasets/ds002345) - Human fMRI during naturalistic spoken-story listening, with BIDS-formatted MRI, metadata, and timing annotations for comparing acoustic or language-model features with brain responses. OpenNeuro data declare CC0, while story audio has separate noncommercial scholarly reuse conditions; participants heard different subsets of stories.

### Spiking Heidelberg Datasets

- [Spiking Heidelberg Datasets](https://zenkelab.org/resources/spiking-heidelberg-datasets-shd/) - Model-generated cochlear spike events from spoken digits (SHD) and speech commands (SSC), supplied as HDF5 files for training and comparing temporal SNN classifiers. The datasets use CC BY 4.0; follow the published partitions and note that SHD's test set mixes held-out speakers with speakers also present in training.

## Where to continue

Use [Comparing brains and models](../topics/README.md#comparing-brains-and-models) to connect measurements to evaluations. The [project suggestions](../projects/README.md) offer bounded ways to formulate a data question; [learning pathways](../start-here/pathways.md) provide background routes.
