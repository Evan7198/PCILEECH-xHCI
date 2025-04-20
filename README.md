# PCILEECH-xHCI  
A simplified xHCI controller emulation implemented based on the specification.  

## **Current Implementation**  
### **1. PIO (Programmed I/O) Implementation**  
- MMIO data is captured from QEMU driver tracing.  
- Register definitions align with both the driver implementation and xHCI specification.  
- All read/write operations strictly follow the documented logs and design specifications.  

### **2. TRB (Transfer Request Block) Implementation**  
- xHCI core operations are handled through TRB queues (e.g., Command Ring, Transfer Ring).  
- TRB transmission/reception logic is implemented to improve emulation accuracy:  
  - **Reception**: Parses TRB fields (e.g., Buffer Pointer, TRB Type, IOC flag).  
  - **Transmission**: Constructs spec-compliant TRBs (e.g., `TRB_TYPE_NORMAL`, `TRB_TYPE_SETUP`).

## **Design Support**
### **Tools**
- WaveDrom
- Mermaid
- Deepseek
### **Specifications**
- xHCI Spec
- pcie 5.0 Spec
- pg054
- USB Spec
