# Interdisciplinary Numerical Methods: Numerical PDEs "Spoke" 18.S191/16.S091

This repository holds materials the second 6-unit "spoke" half of a new MIT course (**Spring 2025**) introducing numerical methods and numerical analysis to a broad audience.   18.S191/16.S091 covers **Numerical PDEs**: Finite Difference and Finite Volume
**Syllabus:**
* Units: 6 (2nd half of term)
* Prerequisites: 18.C330 (“hub”)
* Grading: 60% problem sets, 40% final project

This course focuses on numerical methods for modeling physical systems, especially systems described by partial differential equations (PDEs), with a variety of examples drawn from different areas of science and engineering. Likely topics include:
1. Finite-difference methods: accuracy and implementation.
2. Initial value problems: Convergence, consistency, stiffness, and explicit/implicit methods. Method of lines.
3. Finite volume methods
4. Nonlinear PDEs: split-step and other methods
5. Applications including waves, diffusion, incompressible flow

Students will complete weekly homework assignments, as well as a final project investigating the modeling of a physical system (typically a PDE) not directly covered in class, and/or a numerical method significantly different from those covered in class. 


**Instructor**: [Prof. Qiqi Wang](https://aeroastro.mit.edu/people/qiqi-wang/).

---

# Final Project 

The final project will be an 4-8 page paper (single-column, single-spaced, ideally using the SIAM Journal on Numerical Analysis style template), implementing an algorithm for solving some differential equations, for example, reproducing the result of an existing paper. Your paper should be written for an audience of your peers in the class, and should include example numerical results (by you) from application to a representative problem (small-scale is fine), along with discussion of accuracy, stability, and performance characteristics (both theoretical and experimental).

As with any review-style paper, you are expected to reference the published literature thoroughly, citing both original sources and authoritative reviews or textbooks (rarely web pages), providing a clear historical and theoretical context. Include enough in-text citations to clarify which results come from which sources. (You may reuse diagrams from published works with explicit credit. Not doing so is plagiarism.) Model your writing after academic review papers such as those in SIAM Review or Numerische Mathematik.

A Good Final Project Will Include:

1. An introduction and bibliography, placing the implementation in context:
  
  - What differential equation does it solve?
  - What are the initial / boundary conditions?
  - What algorithm is used to solve the equation, and why is this algorithm chosen?
  - What are the main competing algorithms?
  - What variations or extensions have been proposed?

2. A clear and self-contained description of the implementation, including:

  - Summary of the main equations describing the discretization.
  - Key mathematical properties: order of accuracy, stability, stiffness-handling, etc.
  - Implementation considerations (e.g., time-stepping, gridding, memory use).
  - Visualization of results, time evolution, error growth, etc.
  - Performance characteristics, such as: Error vs. time step (convergence rate).
  - Comparison to competing algorithms (accuracy, efficiency, robustness).
  - Discussion of computational cost: flops, memory, wall time

Your implementation can be in a language of your choice. You should not use others' code for your primary implementation — the goal is to demonstrate your understanding. You may, however, compare to external codes for benchmarking purposes.

What to Submit
- Proposal: Due 5/2, one-page or two pages write up on intended topics and method
- Final paper PDF: In SIAM format or similar, due 5/12
- Code archive: A .zip or .tar.gz file with your source code and a short README file describing what each file does and listing any dependencies.
- Presentation: 10 minutes presentation either on **5/9** or **5/12**

----

**Lectures**: MWF10 in 2-142 (Feb 3 – Mar 31), slides and notes posted below.  Lecture videos posted in [Panopto Video on Canvas](https://canvas.mit.edu/courses/32079/external_tools/369).

**Grading** (all assignments **submitted electronically** via [Gradescope on Canvas](https://canvas.mit.edu/courses/32076/external_tools/369)):
* 50% **4 weekly psets:** due Fridays at midnight: April 11, 18, 25, May 2.
* 50% **final project**: due May 12 (last day of class).

**Collaboration policy:** Talk to anyone you want to and read anything you want to, with two caveats: First, make a solid effort to solve a problem on your own before discussing it with classmates or googling. Second, no matter whom you talk to or what you read, write up the solution on your own, without having their answer in front of you (this includes ChatGPT and similar). (You can use [psetpartners.mit.edu](https://psetpartners.mit.edu/) to find problem-set partners.)

**Teaching Assistant**: [Shania Mitra](https://cse.mit.edu/people/shania-mitra/)

**Office Hours**: Thursday 5pm on [Zoom](https://mit.zoom.us/j/6507969881) (Prof. Wang)

**Resources**: Piazza discussion forum (TO BE CREATED), [math learning center](https://math.mit.edu/learningcenter/), [TSR^2 study/resource room](https://ome.mit.edu/programs/talented-scholars-resource-room-tsr2), [pset partners](https://psetpartners.mit.edu/).

Lecture 1 (31 March): [One Note](https://mitprod-my.sharepoint.com/personal/qiqi_mit_edu/_layouts/15/Doc.aspx?sourcedoc=%7B24321bd2-8c69-451a-b0cc-c2b42aed5743%7D&action=view&wd=target%28C.+Finite+Difference+for+PDE%2F20250331.one%7C1dc15f5c-552e-40b4-bc05-8bee1cd58ae0%2F%29&wdorigin=717) [Colab Notebook](https://colab.research.google.com/drive/1ojJIvUNH38rIfuNeOVjxBcq2wWRdBN8N?usp=sharing) [Combined Notes](https://colab.research.google.com/drive/1vLoVuFqkXZERvQ075OU9aQcz1DXcd8AJ?usp=sharing)
