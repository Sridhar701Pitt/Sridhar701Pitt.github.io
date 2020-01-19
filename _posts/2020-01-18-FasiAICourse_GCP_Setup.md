It was quite difficult setting up the Google cloud Platform Console to be able to start working with the course.
The VM being preemtible frequently gets stopped and it beacame almost impossible to connect to it for a few minutes.
One workaround I found was to create multiple similar instances at different locations and hope that at least one works for a reasonable amount of time before getting preempted. I workd reasonably.
Also there were a few issues conneting to the instance probably because I'm running the notebook from inside a ubuntu VM on a windows OS. I used these two commands and one of them probably solved the issue with connecting to the VM

`gcloud compute instances add-metadata my-fastai-instance-2 --metadata=serial-port-enable=1`

and

'gcloud compute routes create default-internet --destination-range 0.0.0.0/0 --next-hop-gateway default-internet-gateway'

The first one definitely solved some issues connecting to the vm.

I hope the creating multiple instances (though I run only one at a time since I only have 1 gpu quota) each with 200GB of disk wont charge me ridiculous amount of money.

Thats it for now. The connection to the remote host (instance) just lost while typing this post. What a bummer.

Now able to use the sync function of github desktop in my PC