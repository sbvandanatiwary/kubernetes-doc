# Practice Test - Deploy Networking Solution

 

#### Solution

  1. <details>
      <summary>We have deployed an application called app in the default namespace. What is the state of the pod?</summary>

      ```bash
      kubectl get pods
      ```

      Note it is stuck at `ContainerCreating`. It will reamin this way.

      > NotRunning

     </details>

  2. <details>
      <summary>Inspect why the POD is not running.</summary>

      ```bash
      kubectl describe pod app
      ```

      The answer is in the `Events` section. It cannot allocate an IP address, therefore...

      > No network configured

     </details>

  3. <details>
      <summary>Deploy weave-net networking solution to the cluster.</summary>

      Apply the manifest found under the `/root/weave` directory.
     </details>
