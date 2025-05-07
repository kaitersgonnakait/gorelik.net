---
title: "Working with the local filesystem and with S3 in the same code"
date: 2021-01-04
categories: 
 - "blog"
tags: 
 - "code"
 - "opensource"
 - "python"
 - "sshalosh"
layout: "post"
---

As data people, we need to work with files: we use files to save and load data, models, configurations, images, and other things. When possible, I prefer working with local files because it's fast and straightforward. However, sometimes, the production code needs to work with data stored on S What do we do? Until recently, you would have to rewrite multiple parts of the code. But not anymore. I created a [`sshalosh` package](https://pypi.org/project/sshalosh-borisgorelik/) that solves so many problems and spares a lot of code rewriting. Here's how you work with it:

    if work_with_s3:
        s3_config = {
          "s3": {
            "defaultBucket": "bucket",
            "accessKey": "ABCDEFGHIJKLMNOP",
            "accessSecret": "/accessSecretThatOnlyYouKnow"
          }
        }
        
    else:
        s3_config = None
    serializer = sshalosh.Serializer(s3_config)
    
    # Done! From now on, you only need to deal with the business logic, not the house-keeping
    
    # Load data & model
    data = serializer.load_json('data.json')
    model = serializer.load_pickle('model.pkl')
    
    # Update
    data = update_with_new_examples()
    model.fit(data)
    
    # Save updated objects
    serializer.dump_json(data, 'data.json')
    serializer.dump_pickle(model, 'model.pkl')


As simple as that.<br>The package provides the following functions.

- path_exists
- rm
- rmtree
- ls
- oad_pickle, dump_pickle
- load_json, dump_json


There is also a multipurpose `open` function that can open a file in read, write or append mode, and returns a handler to it.

## How to install? How to contribute?

The installation is very simple: `pip install sshalosh-borisgorelik`<br>and you're done. The code lives on GitHub under [http://github.com/bgbg/shalosh](http://github.com/bgbg/shalosh). You are welcome to contribute code, documentation, and bug reports.

## The name is strange, isn't it?

Well, naming is hard. In Hebrew, "shalosh" means "three", so "sshalosh" means s Don't overanalyze this. The GitHub repo doesn't have the extra `s`. My bad
