### stormcos

An image-based operating system with its own Kubernetes, storage and networking, written almost entirely in **Rust**.

#### Core projects

| Project | What it is | Shipped Rust lines |
|---|---|---:|
| [rustkube](https://github.com/glennswest/rustkube) | Kubernetes control plane in Rust: apiserver, controller-manager, scheduler | 31,073 |
| [rustkube-node](https://github.com/glennswest/rustkube-node) | the Kubernetes node agent (kubelet) in Rust | 28,502 |
| [stormblock](https://github.com/glennswest/stormblock) | the storage engine: slabs, copy-on-write clones, ublk and NVMe/TCP, the hub every node's storage runs through | 69,243 |
| [stormd](https://github.com/glennswest/stormd) | process supervisor for the platform's services | 12,256 |
| [fastetcd](https://github.com/glennswest/fastetcd) | an etcd v3-compatible key-value store in Rust (Raft), for the control plane | 18,615 |
| [flowsdn](https://github.com/glennswest/flowsdn) | pod networking (CNI and dataplane) in Rust | 43,264 |
| [stormbootx](https://github.com/glennswest/stormbootx) | a UEFI NVMe/TCP boot extension: boots a machine straight from a remote image, no PXE | 8,661 |

#### UEFI network drivers (Rust, `no_std`)

Loaded by stormbootx so a machine can boot over these NICs with no iPXE:

| Driver | Hardware | Shipped Rust lines |
|---|---|---:|
| [stormnic-ixgbe](https://github.com/glennswest/stormnic-ixgbe) | Intel 82599 / X540 / X552 10 GbE | 4,326 |
| [stormnic-mlx4](https://github.com/glennswest/stormnic-mlx4) | Mellanox ConnectX-3 | 3,584 |
| [stormnic-virtio](https://github.com/glennswest/stormnic-virtio) | virtio-net (VMs) | 2,522 |

*Line counts: shipped code only (no tests, build scripts, comments or blanks).*
