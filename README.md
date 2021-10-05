# Welcome to ekpmeasure 


[![Documentation Status](https://readthedocs.org/projects/ekpmeasure/badge/?version=latest)](http://ekpmeasure.readthedocs.io/?badge=latest)
[![PyPI version fury.io](https://badge.fury.io/py/ekpmeasure.svg)](https://pypi.org/project/ekpmeasure/)
[![PyPI license](https://img.shields.io/pypi/l/ekpmeasure.svg)](https://pypi.org/project/ekpmeasure/)
[![PyPi Downloads](http://pepy.tech/badge/ekpmeasure)](http://pepy.tech/project/ekpmeasure)


Repository of analysis and computer control code for various experiments. 


## Overview

ekpmeasure is a set of control and analysis code designed to help streamline experiments. The basic idea is that in experimental work we often take data from many different sources, store it in different places, have varying degrees meta data associated with the data (even for a single type of data) and somehow(!) we are supposed to make sense of it all. We like to compare across trials, days, experimental conditions, etc. and it is very difficult to keep track of what data is where, and quickly access it when we need it. Often I find that folks end up copying and pasting raw data between excel spreadsheets and if you're not careful you will quickly lose track of which data came from where. This package's goal is to make this all easier. 

You may not find the experimental control code as helpful as it is relatively specific to my research in condensed matter physics (though electrical engineers or similar may find it very useful) but the analysis code is for everyone. 

At the heart of the analysis is the [Dataset](https://ekpmeasure.readthedocs.io/en/latest/ekpmeasure.analysis.html#ekpmeasure.analysis.core.Dataset) class which is a means of manipulating *meta data alone* in order to locate which actual data you want to analyze. [Datasets](https://ekpmeasure.readthedocs.io/en/latest/ekpmeasure.analysis.html#ekpmeasure.analysis.core.Dataset) don't care about what the real data looks like, and they keep track of where different data is stored so it is easy to select which data you want to look at - only then do you retrieve the data. The real data is returned in a [Data](https://ekpmeasure.readthedocs.io/en/latest/ekpmeasure.analysis.html#ekpmeasure.analysis.core.Data) class which allows you to group by parameters, perform calculations and much more.  

I am always improving this repository and if you have suggestions, I appreciate any feedback and or issues (<https://github.com/eparsonnet93/ekpmeasure/issues>)

---
## Installation:

```bash
pip install ekpmeasure
```