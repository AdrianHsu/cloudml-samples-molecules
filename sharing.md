# CloudML Samples

```python
(base) adrianhsu:~/Desktop/cloudml-samples/molecules (master)
$ ./run-cloud --work-dir gs://ahsu-cloudml-samples/cloudml-samples/molecules --project reco-sys-capstone
```

$ conda config --set auto_activate_base false

## dataset

[Chemical table file](https://en.wikipedia.org/wiki/Chemical_table_file#SDF)

```python
(ahsu) adrianhsu:~/Desktop
$ head -n 300 cloudml-samples_molecules_data_00000001_00025000.sdf
1
  -OEChem-10082004193D

 31 30  0     1  0  0  0  0  0999 V2000
    0.3387    0.9262    0.4600 O   0  0  0  0  0  0  0  0  0  0  0  0
    3.4786   -1.7069   -0.3119 O   0  5  0  0  0  0  0  0  0  0  0  0
    1.8428   -1.4073    1.2523 O   0  0  0  0  0  0  0  0  0  0  0  0
    0.4166    2.5213   -1.2091 O   0  0  0  0  0  0  0  0  0  0  0  0
   -2.2359   -0.7251    0.0270 N   0  3  0  0  0  0  0  0  0  0  0  0
   -0.7783   -1.1579    0.0914 C   0  0  0  0  0  0  0  0  0  0  0  0
    0.1368   -0.0961   -0.5161 C   0  0  2  0  0  0  0  0  0  0  0  0
   -3.1119   -1.7972    0.6590 C   0  0  0  0  0  0  0  0  0  0  0  0
   -2.4103    0.5837    0.7840 C   0  0  0  0  0  0  0  0  0  0  0  0
   -2.6433   -0.5289   -1.4260 C   0  0  0  0  0  0  0  0  0  0  0  0
    1.4879   -0.6438   -0.9795 C   0  0  0  0  0  0  0  0  0  0  0  0
    2.3478   -1.3163    0.1002 C   0  0  0  0  0  0  0  0  0  0  0  0
    0.4627    2.1935   -0.0312 C   0  0  0  0  0  0  0  0  0  0  0  0
    0.6678    3.1549    1.1001 C   0  0  0  0  0  0  0  0  0  0  0  0
   -0.7073   -2.1051   -0.4563 H   0  0  0  0  0  0  0  0  0  0  0  0
   -0.5669   -1.3392    1.1503 H   0  0  0  0  0  0  0  0  0  0  0  0
   -0.3089    0.3239   -1.4193 H   0  0  0  0  0  0  0  0  0  0  0  0
   -2.9705   -2.7295    0.1044 H   0  0  0  0  0  0  0  0  0  0  0  0
   -2.8083   -1.9210    1.7028 H   0  0  0  0  0  0  0  0  0  0  0  0
   -4.1563   -1.4762    0.6031 H   0  0  0  0  0  0  0  0  0  0  0  0
   -2.0398    1.4170    0.1863 H   0  0  0  0  0  0  0  0  0  0  0  0
   -3.4837    0.7378    0.9384 H   0  0  0  0  0  0  0  0  0  0  0  0
   -1.9129    0.5071    1.7551 H   0  0  0  0  0  0  0  0  0  0  0  0
   -2.2450    0.4089   -1.8190 H   0  0  0  0  0  0  0  0  0  0  0  0
   -2.3000   -1.3879   -2.0100 H   0  0  0  0  0  0  0  0  0  0  0  0
   -3.7365   -0.4723   -1.4630 H   0  0  0  0  0  0  0  0  0  0  0  0
    1.3299   -1.3744   -1.7823 H   0  0  0  0  0  0  0  0  0  0  0  0
    2.0900    0.1756   -1.3923 H   0  0  0  0  0  0  0  0  0  0  0  0
   -0.1953    3.1280    1.7699 H   0  0  0  0  0  0  0  0  0  0  0  0
    0.7681    4.1684    0.7012 H   0  0  0  0  0  0  0  0  0  0  0  0
    1.5832    2.9010    1.6404 H   0  0  0  0  0  0  0  0  0  0  0  0
  1  7  1  0  0  0  0
  1 13  1  0  0  0  0
  2 12  1  0  0  0  0
  3 12  2  0  0  0  0
  4 13  2  0  0  0  0
  5  6  1  0  0  0  0
  5  8  1  0  0  0  0
  5  9  1  0  0  0  0
  5 10  1  0  0  0  0
  6  7  1  0  0  0  0
  6 15  1  0  0  0  0
  6 16  1  0  0  0  0
  7 11  1  0  0  0  0
  7 17  1  0  0  0  0
  8 18  1  0  0  0  0
  8 19  1  0  0  0  0
  8 20  1  0  0  0  0
  9 21  1  0  0  0  0
  9 22  1  0  0  0  0
  9 23  1  0  0  0  0
 10 24  1  0  0  0  0
 10 25  1  0  0  0  0
 10 26  1  0  0  0  0
 11 12  1  0  0  0  0
 11 27  1  0  0  0  0
 11 28  1  0  0  0  0
 13 14  1  0  0  0  0
 14 29  1  0  0  0  0
 14 30  1  0  0  0  0
 14 31  1  0  0  0  0
M  CHG  2   2  -1   5   1
M  END
> <PUBCHEM_COMPOUND_CID>
1

> <PUBCHEM_CONFORMER_RMSD>
0.6

> <PUBCHEM_CONFORMER_DIVERSEORDER>
2
43
65
46
25
35
57
19
53
42
34
37
41
50
30
14
13
10
56
28
55
22
17
44
52
48
21
7
61
16
66
36
12
32
40
1
24
29
63
47
9
39
60
5
20
31
62
51
4
59
67
8
18
11
33
26
6
27
64
15
58
54
23
38
3
45
49

> <PUBCHEM_MMFF94_PARTIAL_CHARGES>
14
1 -0.43
10 0.5
11 -0.11
12 0.91
13 0.66
14 0.06
2 -0.9
3 -0.9
4 -0.57
5 -1.01
6 0.5
7 0.28
8 0.5
9 0.5

> <PUBCHEM_EFFECTIVE_ROTOR_COUNT>
6

> <PUBCHEM_PHARMACOPHORE_FEATURES>
5
1 2 acceptor
1 3 acceptor
1 4 acceptor
1 5 cation
3 2 3 12 anion

> <PUBCHEM_HEAVY_ATOM_COUNT>
14

> <PUBCHEM_ATOM_DEF_STEREO_COUNT>
0

> <PUBCHEM_ATOM_UDEF_STEREO_COUNT>
1

> <PUBCHEM_BOND_DEF_STEREO_COUNT>
0

> <PUBCHEM_BOND_UDEF_STEREO_COUNT>
0

> <PUBCHEM_ISOTOPIC_ATOM_COUNT>
0

> <PUBCHEM_COMPONENT_COUNT>
1

> <PUBCHEM_CACTVS_TAUTO_COUNT>
1

> <PUBCHEM_CONFORMER_ID>
0000000100000002

> <PUBCHEM_MMFF94_ENERGY>
37.801

> <PUBCHEM_FEATURE_SELFOVERLAP>
25.427

> <PUBCHEM_SHAPE_FINGERPRINT>
1 1 17907859857256425260
13132413 78 18339935856441330356
16945 1 18127404777055172104
17841504 4 18338806718360982307
18410436 195 18412821378365737484
20361792 2 18413103948606886951
20645477 70 18193836175106948431
20653091 64 18337681930618404851
20711985 327 18273495675867710310
20711985 344 18052533275153547866
21041028 32 18342473533857807689
21061003 4 18410298003707379195
21524375 3 17335906067529293413
22112679 90 18128282041358100696
23419403 2 17977062926062270852
23552423 10 18193564595396549919
23557571 272 18127697028774774262
23598294 1 17832149325056171186
2748010 2 18339911658547624660
305870 269 17981602981145137625
31174 14 18192722361058170003
528862 383 18124596637411617035
7364860 26 18197783412505576099
81228 2 18051694343465326048
81539 233 17831573545929999781

> <PUBCHEM_SHAPE_MULTIPOLES>
259.66
4.28
3.04
1.21
1.75
2.55
0.16
-3.13
-0.22
-2.18
-0.56
0.21
0.17
0.09

> <PUBCHEM_SHAPE_SELFOVERLAP>
494.342

> <PUBCHEM_SHAPE_VOLUME>
160.7

> <PUBCHEM_COORDINATE_TYPE>
2
5
10

$$$$
1
  -OEChem-10082004193D

 31 30  0     1  0  0  0  0  0999 V2000
    1.0103    0.9866   -0.5684 O   0  0  0  0  0  0  0  0  0  0  0  0
    0.9765   -3.0591    0.1200 O   0  5  0  0  0  0  0  0  0  0  0  0
    1.9717   -1.2742   -0.8979 O   0  0  0  0  0  0  0  0  0  0  0  0
    2.2610    1.0572    1.3725 O   0  0  0  0  0  0  0  0  0  0  0  0
   -2.5906    0.3010   -0.0681 N   0  3  0  0  0  0  0  0  0  0  0  0
   -1.2651    0.3045   -0.8159 C   0  0  0  0  0  0  0  0  0  0  0  0
   -0.0894    0.4289    0.1516 C   0  0  2  0  0  0  0  0  0  0  0  0
   -2.9835    1.7308    0.2746 C   0  0  0  0  0  0  0  0  0  0  0  0
   -3.6658   -0.3245   -0.9449 C   0  0  0  0  0  0  0  0  0  0  0  0
   -2.4479   -0.5068    1.2137 C   0  0  0  0  0  0  0  0  0  0  0  0
    0.3273   -0.8980    0.7886 C   0  0  0  0  0  0  0  0  0  0  0  0
    1.1789   -1.8274   -0.0880 C   0  0  0  0  0  0  0  0  0  0  0  0
    2.1256    1.2519    0.1722 C   0  0  0  0  0  0  0  0  0  0  0  0
    3.1909    1.8292   -0.7098 C   0  0  0  0  0  0  0  0  0  0  0  0
   -1.2914    1.1235   -1.5449 H   0  0  0  0  0  0  0  0  0  0  0  0
   -1.1940   -0.6328   -1.3817 H   0  0  0  0  0  0  0  0  0  0  0  0
   -0.3247    1.1547    0.9378 H   0  0  0  0  0  0  0  0  0  0  0  0
   -2.2284    2.1715    0.9295 H   0  0  0  0  0  0  0  0  0  0  0  0
   -3.0666    2.3020   -0.6550 H   0  0  0  0  0  0  0  0  0  0  0  0
   -3.9507    1.7074    0.7863 H   0  0  0  0  0  0  0  0  0  0  0  0
   -3.3835   -1.3590   -1.1621 H   0  0  0  0  0  0  0  0  0  0  0  0
   -4.6159   -0.2958   -0.4032 H   0  0  0  0  0  0  0  0  0  0  0  0
   -3.7354    0.2557   -1.8700 H   0  0  0  0  0  0  0  0  0  0  0  0
   -2.2967   -1.5574    0.9569 H   0  0  0  0  0  0  0  0  0  0  0  0
   -1.7557   -0.0482    1.9211 H   0  0  0  0  0  0  0  0  0  0  0  0
   -3.4296   -0.4674    1.7051 H   0  0  0  0  0  0  0  0  0  0  0  0
    0.9400   -0.7132    1.6782 H   0  0  0  0  0  0  0  0  0  0  0  0
   -0.4549   -1.5307    1.1843 H   0  0  0  0  0  0  0  0  0  0  0  0
    3.4332    1.1297   -1.5134 H   0  0  0  0  0  0  0  0  0  0  0  0
    4.0947    2.0035   -0.1189 H   0  0  0  0  0  0  0  0  0  0  0  0
    2.8529    2.7838   -1.1205 H   0  0  0  0  0  0  0  0  0  0  0  0
  1  7  1  0  0  0  0
  1 13  1  0  0  0  0
  2 12  1  0  0  0  0
  3 12  2  0  0  0  0
  4 13  2  0  0  0  0
  5  6  1  0  0  0  0
  5  8  1  0  0  0  0
```

```python
Traceback (most recent call last):
  File "/opt/anaconda3/lib/python3.7/site-packages/apache_beam/internal/pickler.py", line 215, in dumps
    s = dill.dumps(o)
  File "/opt/anaconda3/lib/python3.7/site-packages/dill/_dill.py", line 294, in dumps
    dump(obj, file, protocol, byref, fmode, recurse)#, strictio)
  File "/opt/anaconda3/lib/python3.7/site-packages/dill/_dill.py", line 287, in dump
    pik.dump(obj)
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 437, in dump
    self.save(obj)
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 549, in save
    self.save_reduce(obj=obj, *rv)
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 633, in save_reduce
    save(cls)
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 504, in save
    f(self, obj) # Call unbound method with explicit self
  File "/opt/anaconda3/lib/python3.7/site-packages/apache_beam/internal/pickler.py", line 107, in wrapper
    return fun(pickler, obj)
  File "/opt/anaconda3/lib/python3.7/site-packages/dill/_dill.py", line 1315, in save_type
    obj.__bases__, _dict), obj=obj)
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 638, in save_reduce
    save(args)
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 504, in save
    f(self, obj) # Call unbound method with explicit self
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 786, in save_tuple
    save(element)
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 504, in save
    f(self, obj) # Call unbound method with explicit self
  File "/opt/anaconda3/lib/python3.7/site-packages/apache_beam/internal/pickler.py", line 187, in new_save_module_dict
    return old_save_module_dict(pickler, obj)
  File "/opt/anaconda3/lib/python3.7/site-packages/dill/_dill.py", line 902, in save_module_dict
    StockPickler.save_dict(pickler, obj)
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 856, in save_dict
    self._batch_setitems(obj.items())
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 882, in _batch_setitems
    save(v)
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 504, in save
    f(self, obj) # Call unbound method with explicit self
  File "/opt/anaconda3/lib/python3.7/site-packages/dill/_dill.py", line 1386, in save_function
    obj.__dict__), obj=obj)
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 638, in save_reduce
    save(args)
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 504, in save
    f(self, obj) # Call unbound method with explicit self
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 786, in save_tuple
    save(element)
  File "/opt/anaconda3/lib/python3.7/pickle.py", line 504, in save
    f(self, obj) # Call unbound method with explicit self
  File "/opt/anaconda3/lib/python3.7/site-packages/apache_beam/internal/pickler.py", line 167, in new_save_module_dict
    for m in sys.modules.values():
RuntimeError: dictionary changed size during iteration
```

## pip

```python
(ahsu) adrianhsu:~
$ python3
Python 3.6.12 |Anaconda, Inc.| (default, Sep  8 2020, 17:50:39)
[GCC Clang 10.0.0 ] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
KeyboardInterrupt
>>>
(ahsu) adrianhsu:~/Desktop/cloudml-samples/molecules (master)
$ pip3 install tensorflow==1.15.2 tensorflow-transform==0.24.1 apache-beam==2.24.0 apache-beam[gcp]==2.24.0
```

[https://www.tensorflow.org/tfx/transform/install](https://www.tensorflow.org/tfx/transform/install)

it lists all version mapping

```python
Traceback (most recent call last):
  File "preprocess.py", line 227, in <module>
    work_dir=args.work_dir)
  File "preprocess.py", line 195, in run
    | 'Write transformFn' >> transform_fn_io.WriteTransformFn(work_dir))
  File "/opt/anaconda3/envs/ahsu/lib/python3.6/site-packages/apache_beam/pipeline.py", line 556, in __exit__
    self.result.wait_until_finish()
  File "/opt/anaconda3/envs/ahsu/lib/python3.6/site-packages/apache_beam/runners/dataflow/dataflow_runner.py", line 1633, in wait_until_finish
    self)
apache_beam.runners.dataflow.dataflow_runner.DataflowRuntimeException: Dataflow pipeline failed. State: FAILED, Error:
Traceback (most recent call last):
  File "/usr/local/lib/python3.6/site-packages/dataflow_worker/batchworker.py", line 771, in run
    self._load_main_session(self.local_staging_directory)
  File "/usr/local/lib/python3.6/site-packages/dataflow_worker/batchworker.py", line 512, in _load_main_session
    pickler.load_session(session_file)
  File "/usr/local/lib/python3.6/site-packages/apache_beam/internal/pickler.py", line 307, in load_session
    return dill.load_session(file_path)
  File "/usr/local/lib/python3.6/site-packages/dill/_dill.py", line 368, in load_session
    module = unpickler.load()
  File "/usr/local/lib/python3.6/site-packages/dill/_dill.py", line 472, in load
    obj = StockUnpickler.load(self)
  File "/usr/local/lib/python3.6/site-packages/dill/_dill.py", line 462, in find_class
    return StockUnpickler.find_class(self, module, name)
AttributeError: Can't get attribute 'ValidateInputData' on <module 'dataflow_worker.start' from '/usr/local/lib/python3.6/site-packages/dataflow_worker/start.py'>
```

## sol

```python
class ValidateInputData(beam.DoFn):
  """This DoFn validates that every element matches the metadata given."""
  def __init__(self, feature_spec):
    super(ValidateInputData, self).__init__()
    self.feature_names = set(feature_spec.keys())

-----
class ValidateInputData(beam.DoFn):
  """This DoFn validates that every element matches the metadata given."""
  def __init__(self, feature_spec):
    # super(ValidateInputData, self).__init__()
    self.feature_names = set(feature_spec.keys())

```

```python
Traceback (most recent call last):
  File "preprocess.py", line 229, in <module>
    dump(preprocess_data, os.path.join(args.work_dir, 'PreprocessData'))
  File "preprocess.py", line 56, in dump
    pickle.dump(obj, f, protocol=pickle.HIGHEST_PROTOCOL)
  File "/opt/anaconda3/envs/ahsu/lib/python3.6/site-packages/dill/_dill.py", line 259, in dump
    Pickler(file, protocol, **_kwds).dump(obj)
  File "/opt/anaconda3/envs/ahsu/lib/python3.6/site-packages/dill/_dill.py", line 445, in dump
    StockPickler.dump(self, obj)
  File "/opt/anaconda3/envs/ahsu/lib/python3.6/pickle.py", line 411, in dump
    self.framer.end_framing()
  File "/opt/anaconda3/envs/ahsu/lib/python3.6/pickle.py", line 197, in end_framing
    self.commit_frame(force=True)
  File "/opt/anaconda3/envs/ahsu/lib/python3.6/pickle.py", line 209, in commit_frame
    write(data)
  File "/opt/anaconda3/envs/ahsu/lib/python3.6/site-packages/tensorflow_core/python/lib/io/file_io.py", line 108, in write
    compat.as_bytes(file_content), self._writable_file)
  File "/opt/anaconda3/envs/ahsu/lib/python3.6/site-packages/tensorflow_core/python/util/compat.py", line 71, in as_bytes
    (bytes_or_text,))
TypeError: Expected binary or unicode string, got <memory at 0x7fe09545adc8>
```

[Save a class into a binary file - Python](https://stackoverflow.com/questions/32296146/save-a-class-into-a-binary-file-python)

[How is dill different from Python's pickle module?](https://stackoverflow.com/questions/58193119/how-is-dill-different-from-pythons-pickle-module)

```python
>> Training
$ gcloud ai-platform jobs submit training cloudml_samples_molecules_20201024_000808 --module-name trainer.task --package-path trainer --staging-bucket gs://ahsu-cloudml-samples --runtime-version 1.13 --region us-central1 --stream-logs -- --work-dir gs://ahsu-cloudml-samples/cloudml-samples/molecules
API [ml.googleapis.com] not enabled on project [622188232773]. Would
you like to enable and retry (this will take a few minutes)? (y/N)?

Enabling service [ml.googleapis.com] on project [622188232773]...
Operation "operations/acf.4eede915-4608-4741-8aed-6be97ec03016" finished successfully.
ERROR: (gcloud.ai-platform.jobs.submit.training) FAILED_PRECONDITION: Field: package_uris Error: The provided GCS paths cannot be read by service account service-622188232773@cloud-ml.google.com.iam.gserviceaccount.com. If you just enabled the API, please try again after a few minutes.
- '@type': type.googleapis.com/google.rpc.BadRequest
  fieldViolations:
  - description: The provided GCS paths cannot be read by service account service-622188232773@cloud-ml.google.com.iam.gserviceaccount.com.
      If you just enabled the API, please try again after a few minutes.
    field: package_uris
```

[Runtime version list | AI Platform Training | Google Cloud](https://cloud.google.com/ai-platform/training/docs/runtime-version-list)

```python
"DEPRECATION: Python 2.7 reached the end of its life on January 1st, 2020. Please upgrade your Python as Python 2.7 is no longer maintained. pip 21.0 will drop support for Python 2.7 in January 2021. More details about Python 2 support in pip, can be found at https://pip.pypa.io/en/latest/development/release-process/#python-2-support"
"ERROR: Could not find a version that satisfies the requirement tensorflow-transform==0.24.1 (from molecules==0.0.1) (from versions: 0.1.0, 0.1.1, 0.1.2, 0.1.3, 0.1.4, 0.1.5, 0.1.6, 0.1.7, 0.1.8, 0.1.9, 0.1.10, 0.3.0, 0.3.1, 0.4.0, 0.5.0, 0.6.0, 0.8.0, 0.9.0, 0.11.0, 0.12.0, 0.13.0, 0.14.0, 0.15.0, 0.21.0, 0.21.2)"
```

```python
(ahsu) adrianhsu:~/Desktop/cloudml-samples/molecules (master)
$ pip3 install tensorflow==1.15.0 tensorflow-transform==0.21.2 apache-beam==2.17.0 apache-beam[gcp]==2.17.0
```

```python
master-replica-0"Traceback (most recent call last):
  File "/usr/lib/python2.7/runpy.py", line 174, in _run_module_as_main
    "__main__", fname, loader, pkg_name)
  File "/usr/lib/python2.7/runpy.py", line 72, in _run_code
    exec code in run_globals
  File "/root/.local/lib/python2.7/site-packages/trainer/task.py", line 202, in <module>
    preprocess_data = load(os.path.join(args.work_dir, 'PreprocessData'))
  File "/root/.local/lib/python2.7/site-packages/trainer/task.py", line 116, in load
    return pickle.load(f)
  File "/root/.local/lib/python2.7/site-packages/dill/_dill.py", line 305, in load
    obj = pik.load()
  File "/usr/lib/python2.7/pickle.py", line 864, in load
    dispatch[key](self)
  File "/usr/lib/python2.7/pickle.py", line 892, in load_proto
    raise ValueError, "unsupported pickle protocol: %d" % proto
ValueError: unsupported pickle protocol: 4
"
```

[Managing runtime versions | AI Platform Training | Google Cloud](https://cloud.google.com/ai-platform/training/docs/versioning)

```python
The replica master 0 exited with a non-zero status of 1. 
Traceback (most recent call last):
  File "/usr/lib/python3.7/runpy.py", line 193, in _run_module_as_main
    "__main__", mod_spec)
  File "/usr/lib/python3.7/runpy.py", line 85, in _run_code
    exec(code, run_globals)
  File "/root/.local/lib/python3.7/site-packages/trainer/task.py", line 202, in <module>
    preprocess_data = load(os.path.join(args.work_dir, 'PreprocessData'))
  File "/root/.local/lib/python3.7/site-packages/trainer/task.py", line 116, in load
    return pickle.load(f)
  File "/root/.local/lib/python3.7/site-packages/dill/_dill.py", line 305, in load
    obj = pik.load()
  File "/root/.local/lib/python3.7/site-packages/dill/_dill.py", line 474, in find_class
    return StockUnpickler.find_class(self, module, name)
AttributeError: Can't get attribute 'PreprocessData' on <module 'trainer.task' from '/root/.local/lib/python3.7/site-packages/trainer/task.py'>

To find out more about why your job exited please check the logs: https://console.cloud.google.com/logs/viewer?project=622188232773&resource=ml_job%2Fjob_id%2Fcloudml_samples_molecules_20201024_005506&advancedFilter=resource.type%3D%22ml_job%22%0Aresource.labels.job_id%3D%22cloudml_samples_molecules_20201024_005506%22
```

### Sol: add this to task.py

```python
class PreprocessData(object):
  def __init__(
      self,
      input_feature_spec,
      labels,
      train_files_pattern,
      eval_files_pattern):
  
    self.labels = labels
    self.input_feature_spec = input_feature_spec
    self.train_files_pattern = train_files_pattern
    self.eval_files_pattern = eval_files_pattern
```

### timeline

Creation time
Oct 24, 2020, 11:07:44 AM
Start time
Oct 24, 2020, 11:08:38 AM
End time
Oct 24, 2020, 11:13:10 AM

11:24 log shown on my local pc

```python
INFO	2020-10-24 11:10:39 -0700	master-replica-0		Restoring parameters from gs://ahsu-cloudml-samples/cloudml-samples/molecules/model/model.ckpt-1000
INFO	2020-10-24 11:10:39 -0700	master-replica-0		Running local_init_op.
INFO	2020-10-24 11:10:39 -0700	master-replica-0		Done running local_init_op.
INFO	2020-10-24 11:10:40 -0700	master-replica-0		Evaluation [10/100]
INFO	2020-10-24 11:10:40 -0700	master-replica-0		Evaluation [20/100]
INFO	2020-10-24 11:10:40 -0700	master-replica-0		Evaluation [30/100]
INFO	2020-10-24 11:10:40 -0700	master-replica-0		Evaluation [40/100]
INFO	2020-10-24 11:10:40 -0700	master-replica-0		Evaluation [50/100]
INFO	2020-10-24 11:10:40 -0700	master-replica-0		Evaluation [60/100]
INFO	2020-10-24 11:10:40 -0700	master-replica-0		Evaluation [70/100]
INFO	2020-10-24 11:10:40 -0700	master-replica-0		Evaluation [80/100]
INFO	2020-10-24 11:10:40 -0700	master-replica-0		Evaluation [90/100]
INFO	2020-10-24 11:10:40 -0700	master-replica-0		Evaluation [100/100]
INFO	2020-10-24 11:10:40 -0700	master-replica-0		Finished evaluation at 2020-10-24-18:10:40
INFO	2020-10-24 11:10:40 -0700	master-replica-0		Saving dict for global step 1000: average_loss = 429.37677, global_step = 1000, label/mean = 48.35188, loss = 27480.113, prediction/mean = 53.79005
INFO	2020-10-24 11:10:41 -0700	master-replica-0		Saving 'checkpoint_path' summary for global step 1000: gs://ahsu-cloudml-samples/cloudml-samples/molecules/model/model.ckpt-1000
INFO	2020-10-24 11:10:42 -0700	master-replica-0		Performing the final export in the end of training.
WARNING	2020-10-24 11:10:43 -0700	master-replica-0		From /root/.local/lib/python3.7/site-packages/trainer/task.py:113: The name tf.placeholder is deprecated. Please use tf.compat.v1.placeholder instead.
INFO	2020-10-24 11:10:43 -0700	master-replica-0		Saver not created because there are no variables in the graph to restore
INFO	2020-10-24 11:10:43 -0700	master-replica-0		Calling model_fn.
INFO	2020-10-24 11:10:43 -0700	master-replica-0		Done calling model_fn.
WARNING	2020-10-24 11:10:43 -0700	master-replica-0		From /root/.local/lib/python3.7/site-packages/tensorflow_core/python/saved_model/signature_def_utils_impl.py:201: build_tensor_info (from tensorflow.python.saved_model.utils_impl) is deprecated and will be removed in a future version.
WARNING	2020-10-24 11:10:43 -0700	master-replica-0		Instructions for updating:
WARNING	2020-10-24 11:10:43 -0700	master-replica-0		This function will only be available through the v1 compatibility library as tf.compat.v1.saved_model.utils.build_tensor_info or tf.compat.v1.saved_model.build_tensor_info.
INFO	2020-10-24 11:10:43 -0700	master-replica-0		Signatures INCLUDED in export for Classify: None
INFO	2020-10-24 11:10:43 -0700	master-replica-0		Signatures INCLUDED in export for Regress: None
INFO	2020-10-24 11:10:43 -0700	master-replica-0		Signatures INCLUDED in export for Predict: ['predict']
INFO	2020-10-24 11:10:43 -0700	master-replica-0		Signatures INCLUDED in export for Train: None
INFO	2020-10-24 11:10:43 -0700	master-replica-0		Signatures INCLUDED in export for Eval: None
INFO	2020-10-24 11:10:43 -0700	master-replica-0		Signatures EXCLUDED from export because they cannot be be served via TensorFlow Serving APIs:
INFO	2020-10-24 11:10:43 -0700	master-replica-0		'serving_default' : Regression input must be a single string Tensor; got {'TotalC': <tf.Tensor 'TotalC:0' shape=(?,) dtype=int64>, 'TotalH': <tf.Tensor 'TotalH:0' shape=(?,) dtype=int64>, 'TotalO': <tf.Tensor 'TotalO:0' shape=(?,) dtype=int64>, 'TotalN': <tf.Tensor 'TotalN:0' shape=(?,) dtype=int64>}
INFO	2020-10-24 11:10:43 -0700	master-replica-0		'regression' : Regression input must be a single string Tensor; got {'TotalC': <tf.Tensor 'TotalC:0' shape=(?,) dtype=int64>, 'TotalH': <tf.Tensor 'TotalH:0' shape=(?,) dtype=int64>, 'TotalO': <tf.Tensor 'TotalO:0' shape=(?,) dtype=int64>, 'TotalN': <tf.Tensor 'TotalN:0' shape=(?,) dtype=int64>}
WARNING	2020-10-24 11:10:43 -0700	master-replica-0		Export includes no default signature!
INFO	2020-10-24 11:10:43 -0700	master-replica-0		Restoring parameters from gs://ahsu-cloudml-samples/cloudml-samples/molecules/model/model.ckpt-1000
INFO	2020-10-24 11:10:44 -0700	master-replica-0		Assets added to graph.
INFO	2020-10-24 11:10:44 -0700	master-replica-0		No assets to write.
INFO	2020-10-24 11:10:48 -0700	master-replica-0		SavedModel written to: gs://ahsu-cloudml-samples/cloudml-samples/molecules/model/export/final/temp-b'1603563042'/saved_model.pb
INFO	2020-10-24 11:10:50 -0700	master-replica-0		Loss for final step: 32476.467.
INFO	2020-10-24 11:10:50 -0700	master-replica-0		gs://ahsu-cloudml-samples/cloudml-samples/molecules/PreprocessData
INFO	2020-10-24 11:10:51 -0700	master-replica-0		Module completed; cleaning up.
INFO	2020-10-24 11:10:51 -0700	master-replica-0		Clean up finished.
INFO	2020-10-24 11:10:51 -0700	master-replica-0		Task completed successfully.
INFO	2020-10-24 11:13:10 -0700	service		Job completed successfully.
```

### pred

```python
endTime: '2020-10-24T11:13:10'
jobId: cloudml_samples_molecules_20201024_110740
startTime: '2020-10-24T11:08:38'
state: SUCCEEDED

Model: gs://ahsu-cloudml-samples/cloudml-samples/molecules/model/export/final/1603563042/

>> Batch prediction
$ python predict.py --work-dir gs://ahsu-cloudml-samples/cloudml-samples/molecules --model-dir gs://ahsu-cloudml-samples/cloudml-samples/molecules/model/export/final/1603563042/ batch --project reco-sys-capstone --runner DataflowRunner --temp_location gs://ahsu-cloudml-samples/cloudml-samples/molecules/beam-temp --setup_file ./setup.py --inputs-dir gs://ahsu-cloudml-samples/cloudml-samples/molecules/data --outputs-dir gs://ahsu-cloudml-samples/cloudml-samples/molecules/predictions
```

```python
class Predict(beam.DoFn):
  def __init__(self,
      model_dir,
      id_key,
      meta_tag='serve',
      meta_signature='predict',
      meta_predictions='predictions'):
    # super(Predict, self).__init__() # remember to comment this
```