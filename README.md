# fastapi_tinyLlama_genai
If you have this error when running the server
'''
RuntimeError: Failed to import transformers.pipelines because of the following error (look up to see its traceback): Failed to import transformers.generation.utils because of the following error (look up to see its traceback): numpy.dtype size changed, may indicate binary incompatibility. Expected 96 from C header, got 88 from PyObject
'''
This means that some installed packages were compiled against a different NumPy version. 

To fix it..

pip uninstall -y numpy
pip install numpy==1.26.4
