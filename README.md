# cka-config
CKA configuration re: https://github.com/ismet55555/Certified-Kubernetes-Administrator-Notes

The following are some example usages:

k get nodes -o wide

kc deploymentmy my-dep --image=nginx --replicas=3

kr-dry my-pod --image=nginx --command sleep 36000

kr-dry --image=busybox -- "/bin/sh" "-c" "sleep 36000"

---

Terminal Command Completion
The following is useful so that you can use the TAB key to auto-complete a command, allowing you to not always have to remember the exact keyword or spelling.

Type the following into the terminal:

kubectl completion bash >> ~/.bashrc - kubectl command completion

kubeadm completion bash >> ~/.bashrc - kubeadm command completion

exec $SHELL - Reload shell to enable all added completion

Also know VIM basics:

vim my-file.yaml - If file exists, open it, else create it for editing

:w - Save

:x - Save and exit

:q - Exit

:q! - Exit without saving

i - Insert mode, regular text editor mode

v - Visual mode for selection

ESC - Normal mode

tmux
tmux will allow you to use multiple terminal windows in one (aka terminal multiplexing). Make sure you know the basics for tmux usage:

NOTE: CTRL + b is the prefix to anything in tmux

tmux - Turn and enter tmux

CTRL + b " - Split the window vertically (line is horizontal)

CTRL + b % - Split the window horizontally (line is vertical)

CTRL + b <ARROW KEY> - Switch between window panes
  
CTRL + b (hold) <ARROW KEY> - Resize current window pane
  
CTRL + d or exit - Close a window pane
  
... More (if needed): https://gist.github.com/ismet55555/f78cecaab16d7a0acf786ab6b11c7d56
  
  Mouse Support (Optional)
  
If you want to be able to click and select within tmux and tmux panes, you can also enable mouse support. This can be useful.

These steps must be done outside of tmux

Create a .tmux.conf file and edit it

vim ~/.tmux.conf
  
Add the configuration, save, and exit file

set -g mouse on
  
Reload tmux configuration

tmux source .tmux.conf
