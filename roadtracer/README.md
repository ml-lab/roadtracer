RoadTracer
==========

Training
--------

First, if you used different paths for the imagery/graphs/json when preparing the dataset, then update the paths at the top of `tileloader.py`.

Now we can train the model.

	mkdir /data/model/
	mkdir /data/model/model_latest
	mkdir /data/model/model_best
	python train.py /data/model/


Inference
---------

First, update `infer.py` (`MODEL_PATH`, `REGION`, and `TILE_START`/`TILE_END`).

Then:

	python infer.py /data/model/model_latest/model out.graph

This will output `out.graph`.
