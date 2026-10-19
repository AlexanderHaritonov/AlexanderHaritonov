# 👋 Alexander Haritonov

**Algorithm & Software Engineer | Computer Vision & 3D Depth | Evaluation & Benchmarking**.  

---

## Projects

### ⭐ Check out my latest released project
[Mask2PolyMin](https://github.com/AlexanderHaritonov/Mask2PolyMin) — turn noisy raster segmentation masks into clean polygons with a minimal number of segments.
If you find it useful, a star helps others discover it!

![GitHub stars](https://img.shields.io/github/stars/AlexanderHaritonov/Mask2PolyMin?style=social)

### OpenCV: faster `convexHull` via a measured sort dispatcher
`cv::convexHull` spent most of its time in `std::sort` (O(n log n)), even though the hull algorithm itself is linear. Together with a mentee from Kamatech, I replaced the sort with a dispatcher that picks the fastest method for each input:

- **Counting sort** when the coordinate range is small relative to the point count
- **Radix sort** (stable, 8-bit digits) when there are enough points per pass
- **`std::sort`** otherwise

| Input | Speedup vs. `std::sort` |
|---|---|
| Noisy closed contours, 16–50,000 points | up to 6.4x |
| Dense random points, up to 50,000 | up to 66x |
| Tiny contours (16–32 points) | ~1x (no regression beyond noise) |

[Issue #28846](https://github.com/opencv/opencv/issues/28846)
[PR #28868](https://github.com/opencv/opencv/pull/28868) (mentee's bucket sort; fixes and improvements by me)·
[PR #30196](https://github.com/opencv/opencv/pull/30196) (a follow-up: dispatcher, radix sort, float support) · both under review

### Depth evaluation: stereo vs. mono vs. LiDAR (KITTI)

How far can you trust camera-based depth? I compared stereo (OpenCV SGBM) and monocular depth (Depth Anything V2) against LiDAR ground truth on KITTI drives.
Built during the [3D Ascension](https://www.thinkautonomous.ai/) program by Think Autonomous.
- **[bev_from_depth](https://github.com/AlexanderHaritonov/bev_from_depth):** bird's-eye occupancy maps from each source, scored by IoU per distance band. 
- **[mono_vs_stereo_vs_lidar](https://github.com/AlexanderHaritonov/mono_vs_stereo_vs_lidar):** per-frame RMSE and nearest distance per detected person or car, compared with LiDAR.

---

## 🚀 Highlights

- 📊 Expertise in **computer vision, 3D/depth, computational geometry, combinatorics, graph and route planning**  
- 💡 Worked on Excel Copilot at Microsoft (2024–25)
- 🏆 Winner of **RWTH Aachen Programming Competition for Students** (sponsored by Sun Microsystems)  

---



## 🛠️ Tech Stack

- **Languages:** Python, C, C++, C#, TypeScript  
- **Domains:** Computer Vision, Maps, Computational Geometry, Graph Algorithms 
- **Frameworks & Tools:** OpenCV, NumPy

---

## 📫 Connect with Me

- 💼 [LinkedIn](https://www.linkedin.com/in/alexanderharitonov/)
- 🧑‍💻 [GitHub](https://github.com/AlexanderHaritonov)
