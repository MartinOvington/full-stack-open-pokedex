The example project is a Raytracing program written in C++.

The first step in the CI process will be to run all files through a linter that checks that the code conforms to a specific set of style rules. An example is CPPLint, which enforces Google's C++ style guide. The team could create a set of unit tests that C++ modules have to pass. In addition you could create reference images that the Raytracer build has to match as a form of integration testing, although this would only be useable if the proposed changes aren't meant to change the output images. The build process can be specified in a common Make file, that can use a specific version of a compiler e.g. GCC.

An alternative CI to GitHub Actions and Jenkins, is Travis CI. Travis CI is a continuous integration service for testing and building software on GitHub and Bitbucket. It is configured used a .travil.yml file in the root of the repository. Travis CI works with many languages, including C++, which makes it suitable for the example projoect above.

The example project may be more economical to run on a self-hosted service, due to the CPU intensive nature of Raytracing. The tests that would need to be run may take a lot of CPU minutes. However, this depends on how frequently the code needs to be tested, the cost of the Cloud services and the expected length of time that the code will continue to be worked on.

- Event trigger here -
