# 3DORB.github.io

This is a temporary website for the work "Real-World 3D Object Inverse Rendering Benchmark", a.k.a. 3D-ORB.

Our dataset is available [here](https://drive.google.com/drive/folders/1_BiGs_pPenRJfAwI_9eNv4ZRJLZCKObU?usp=sharing).

Our evaluation code is available [here](https://github.com/3DORB/3dorb).

Our raw data and data processing scripts will be available soon.

Structure of our dataset:
```
data	
----- \<obj_name\>_scene00x
    ----- blender_HDR/LDR				
    ----- test/%04d.{exr/png}       (Test images in HDR/LDR)	
    ----- test_mask/%04d.png        (Test mask images in LDR)	
    ----- train/%04d.{exr/png}      (Train images in HDR/LDR)	
    ----- train_mask/%04d.png       (Train mask images in LDR)	
    ----- transforms_test.json      (Test metadata)	
    ----- transforms_train.json     (Train metadata)	
    ----- transforms_novel.json     (metadata of novel scene test images. Note that each frame has a unique camera angle)				
----- llff_HDR/LDR				
    ----- images/%04d.{exr/png}     (All images in HDR/LDR)
    ----- masks/%04d.png            (All image masks in LDR)
    ----- sparse/0/*.bin            (Colmap Files)	
    ----- sparse/\<scene\>/*.bin    (Colmap Files of novel scenes)	
    ----- poses_bounds.npy          (LLFF's camera files)	
    ----- train_id.txt              (name of training images)	
    ----- test_id.txt               (name of test images)	
    ----- novel_id.txt              (name of test images from novel scenes)	
    ----- poses_bounds_novel.npy    (camera poses of novel scene test images (indexed by order of names in novel_id.txt)					
----- ground_truth				
    ----- env_map/%04d.exr          (Ground truth HDRI environment maps (share the same name with the corresponding test image))
    ----- surface_normal/%04d.npy   (Ground truth surface normal maps)
    ----- z_depth/%04d.npy          (Ground truth Z-depth maps)
    ----- pseudo_gt_albedo/%04d.npy (Pseudo GT albedo maps)
    ----- mesh_blender/mesh.obj     (Scanned Mesh aligned with the blender format data)
```
