## System Interaction Flow: Python Tensor Computation on GPU

```plaintext
You (user)
   ↓
Write Python Code using PyTorch
   ↓
[Python Interpreter]
   ↓
Call PyTorch API (e.g., torch.randn(..., device="cuda"))
   ↓
[PyTorch Frontend (Python)] 
   ↓
Calls C++ Backend (LibTorch / ATen)
   ↓
Invokes CUDA Runtime APIs
   ↓
NVIDIA GPU Driver (via OS Kernel)
   ↓
[GPU Hardware Executes the Tensor Operation]