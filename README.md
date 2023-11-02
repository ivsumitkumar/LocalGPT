# LocalGPT
ingest your own file and talk with it


# Use the device type argument to specify a given device. To run on cpu

```sh
python ingest.py --device_type cpu
```

# 1. Local File Ingestion
  - 1. Put the file in SOURCE_DOCUMENTS folder
  - 2. Run the command to start file ingestion.

```sh
python ingest.py
```

  - If your device doesn't have GPU, execute the following command to run on cpu
```sh
python ingest.py --device_type cpu
```
To run on `M1/M2`

```sh
python ingest.py --device_type mps
```

Use help for a full list of supported devices.

```sh
python ingest.py --help
```

This will create a new folder called `DB` and use it for the newly created vector store. You can ingest as many documents as you want, and all will be accumulated in the local embeddings database.
If you want to start from an empty database, delete the `DB` and reingest your documents.

Note: When you run this for the first time, it will need internet access to download the embedding model (default: `Instructor Embedding`). In the subsequent runs, no data will leave your local environment and you can ingest data without internet connection.