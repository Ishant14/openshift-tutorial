Openshift is a RedHat's opensource container platform for developing and hosting enterprise grade applicaition. 
OpenShift is a redhat platform as a service , which mean once we deploy the application ,it take care of the managing the 
unnderlying component thereby letting the developer on coding only.

**Openshift has four different flavours :**

1) OpenShift origin 
2) OpenShift Online 
3) OpenShift dedicated 
4) OpenShift Enterprise 


**Why do we need containerize solution ?**

Containers are a solution to the problem of how to get software to run reliably when moved from one computing environment to another. This could be from a developer's laptop to a test environment, from a staging environment into production, and perhaps from a physical machine in a data center to a virtual machine in a private or public cloud.

Problems arise when the supporting software environment is not identical, says Docker  creator Solomon Hykes. "You're going to test using Python 2.7, and then it's going to run on Python 3 in production and something weird will happen. Or you'll rely on the behavior of a certain version of an SSL library and another one will be installed. You'll run your tests on Debian and production is on Red Hat and all sorts of weird things happen."

And it's not just different software that can cause problems, he added. "The network topology might be different, or the security policies and storage might be different but the software has to run on it."

**How do containers solve this problem?**

Put simply, a container consists of an entire runtime environment: an application, plus all its dependencies, libraries and other binaries, and configuration files needed to run it, bundled into one package. By containerizing the application platform and its dependencies, differences in OS distributions and underlying infrastructure are abstracted away.

**What's the difference between containers and virtualization?**

  1) With virtualization technology, the package that can be passed around is a virtual machine, and it includes an entire operating system as well as the application. A physical server running three virtual machines would have a hypervisor and three separate operating systems running on top of it.

By contrast a server running three containerized applications with Docker runs a single operating system, and each container shares the operating system kernel with the other containers. Shared parts of the operating system are read only, while each container has its own mount (i.e., a way to access the container) for writing. That means the containers are much more lightweight and use far fewer resources than virtual machines.


2) A container may be only tens of megabytes in size, whereas a virtual machine with its own entire operating system may be several gigabytes in size. Because of this, a single server can host far more containers than virtual machines.

3) Another major benefit is that virtual machines may take several minutes to boot up their operating systems and begin running the applications they host, while containerized applications can be started almost instantly. That means containers can be instantiated in a "just in time" fashion when they are needed and can disappear when they are no longer required, freeing up resources on their hosts.

4) Containerization allows for greater modularity. Rather than run an entire complex application inside a single container, the application can be split in to modules (such as the database, the application front end, and so on). This is the so-called microservices approach.  Applications built in this way are easier to manage because each module is relatively simple, and changes can be made to modules without having to rebuild the entire application. Because containers are so lightweight, individual modules (or microservices) can be instantiated only when they are needed and are available almost immediatel

**How secure are conatiners ?**

Many people believe that containers are less secure than virtual machines because if there's a vulnerability in the container host kernel, it could provide a way into the containers that are sharing it. That's also true with a hypervisor, but since a hypervisor provides far less functionality than a Linux kernel (which typically implements file systems, networking, application process controls and so on) it presents a much smaller attack surface.

But in the last couple of years a great deal of effort has been devoted to developing software to enhance the security of containers.

For example, Docker (and other container systems) now include a signing infrastructure allowing administrators to sign container images to prevent untrusted containers from being deployed.

However, it is not necessarily the case that a trusted, signed container is secure to run, because vulnerabilities may be discovered in some of the software in the container after it has been signed. For that reason, Docker and others offer container security scanning solutions that can notify administrators if any container images have vulnerabilities that could be exploited.

More specialized container security software has also been developed. For example, Twistlock offers software that profiles a container's expected behavior and "whitelists" processes, networking activities (such as source and destination IP addresses and ports) and even certain storage practices so that any malicious or unexpected behavior can be flagged.

Another specialist container security company called Polyverse takes a different approach. It takes advantage of the fact that containers can be started in a fraction of a second to relaunch containerized applications in a known good state every few seconds to minimize the time that a hacker has to exploit an application running in a container.


**How to run Linux container on windows Server ?**

With LCOW, the Docker daemon runs as a Windows process (same as when running Docker Windows containers), and every time you start a Linux container Docker launches a minimal Hyper-V hypervisor running a VM with a Linux kernel, runc and the container processes running on top.

Because there’s only one Docker daemon, and because that daemon now runs on Windows, it will soon be possible to run Windows and Linux Docker containers side-by-side, in the same networking namespace. This will unlock a lot of exciting development and production scenarios for Docker users on Windows.


**How doeos Kubernetes help ?** 

Kubernetes is an open-source system for automating deployment, scaling, and management of containerized applications.




1) An enterprise application  has to go through different  environment like DEV, TEST, UAT before going to production.
2) Setting up each environment requires a lot of effort like we have to do the required configuration on each of the environment, all the required libraries has to be maintained for each of them.
3) Mostly it has been seen that due to different security cocnern , DEV has different libraries and UAT has different confiuration and libraries which has created a lot of problem for the developers.
4) A whole team has to create to take care of the complete end to end funcitonality. 
5) Still feasible for moniolithic application but becomes very difficult to maintain the same when we go for the microservices architecture. 




