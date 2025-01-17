1. **`addi sp, sp, -16`**  
   - Opcode (I-Type): `0010011`  
   - Registers: `rd = sp (x2)`, `rs1 = sp (x2)`  
   - Immediate: `-16 (111111111000 in 2's complement)`  
   - Breakdown:  
     - **imm[11:0]**: `111111111000`  
     - **rs1 (sp)**: `00010`  
     - **funct3**: `000`  
     - **rd (sp)**: `00010`  
     - **opcode**: `0010011`  

---

2. **`sd ra, 8(sp)`**  
   - Opcode (S-Type): `0100011`  
   - Registers: `rs2 = ra (x1)`, `rs1 = sp (x2)`  
   - Immediate: `8 (0000000001000)`  
   - Breakdown:  
     - **imm[11:5]**: `0000000`  
     - **rs2 (ra)**: `00001`  
     - **rs1 (sp)**: `00010`  
     - **funct3**: `011`  
     - **imm[4:0]**: `01000`  
     - **opcode**: `0100011`  

---

3. **`lui s0, 0x21`**  
   - Opcode (U-Type): `0110111`  
   - Register: `rd = s0 (x8)`  
   - Immediate: `0x21 (0000000000100001)`  
   - Breakdown:  
     - **imm[31:12]**: `0000000000100001`  
     - **rd (s0)**: `01000`  
     - **opcode**: `0110111`  

---

4. **`jal ra, 1095c <printf>`**  
   - Opcode (J-Type): `1101111`  
   - Register: `rd = ra (x1)`  
   - Offset: `1095c (calculated relative offset, 21 bits)`  
   - Breakdown:  
     - **imm[20]**: `1`  
     - **imm[10:1]**: `1001001011`  
     - **imm[11]**: `1`  
     - **imm[19:12]**: `0100000100`  
     - **rd (ra)**: `00001`  
     - **opcode**: `1101111`  

---

5. **`mv a1, a0`**  
   - Opcode (R-Type): `0110011`  
   - Registers: `rd = a1 (x11)`, `rs1 = a0 (x10)`, `rs2 = x0`  
   - funct3: `000` | funct7: `0000000`  
   - Breakdown:  
     - **funct7**: `0000000`  
     - **rs2**: `00000`  
     - **rs1 (a0)**: `01010`  
     - **funct3**: `000`  
     - **rd (a1)**: `01011`  
     - **opcode**: `0110011`  

---

6. **`li a0, 0`**  
   - Opcode (I-Type): `0010011`  
   - Register: `rd = a0 (x10)`  
   - Immediate: `0`  
   - Breakdown:  
     - **imm[11:0]**: `000000000000`  
     - **rs1 (x0)**: `00000`  
     - **funct3**: `000`  
     - **rd (a0)**: `01010`  
     - **opcode**: `0010011`  

---

7. **`ld ra, 8(sp)`**  
   - Opcode (I-Type): `0000011`  
   - Registers: `rd = ra (x1)`, `rs1 = sp (x2)`  
   - Immediate: `8`  
   - Breakdown:  
     - **imm[11:0]**: `000000001000`  
     - **rs1 (sp)**: `00010`  
     - **funct3**: `011`  
     - **rd (ra)**: `00001`  
     - **opcode**: `0000011`  

---

8. **`slli a0, a0, 0x20`**  
   - Opcode (R-Type): `0110011`  
   - Registers: `rd = a0 (x10)`, `rs1 = a0 (x10)`, `rs2 = x20`  
   - funct3: `001` | funct7: `0000000`  
   - Breakdown:  
     - **funct7**: `0000000`  
     - **rs2**: `10100`  
     - **rs1 (a0)**: `01010`  
     - **funct3**: `001`  
     - **rd (a0)**: `01010`  
     - **opcode**: `0110011`  

---

9. **`sext.w a0, a0`**  
   - Opcode (R-Type): `0111011`  
   - Registers: `rd = a0 (x10)`, `rs1 = a0 (x10)`  
   - funct7: `0100000` | funct3: `000`  
   - Breakdown:  
     - **funct7**: `0100000`  
     - **rs2**: `00000`  
     - **rs1 (a0)**: `01010`  
     - **funct3**: `000`  
     - **rd (a0)**: `01010`  
     - **opcode**: `0111011`  

---

10. **`jr t0`**  
    - Opcode (I-Type): `1100111`  
    - Register: `rs1 = t0 (x5)`  
    - Immediate: `0`  
    - Breakdown:  
      - **imm[11:0]**: `000000000000`  
      - **rs1 (t0)**: `00101`  
      - **funct3**: `000`  
      - **rd (x0)**: `00000`  
      - **opcode**: `1100111`  

---

11. **`beq a1, t0, 10338 <__moddi3+0x30>`**  
    - Opcode (B-Type): `1100011`  
    - Registers: `rs1 = a1 (x11)`, `rs2 = t0 (x5)`  
    - Offset: `10338 (calculated as a 12-bit signed offset)`  
    - Breakdown:  
      - **imm[12]**: `1`  
      - **imm[10:5]**: `100011`  
      - **rs2 (t0)**: `00101`  
      - **rs1 (a1)**: `01011`  
      - **funct3**: `000`  
      - **imm[4:1]**: `0011`  
      - **imm[11]**: `1`  
      - **opcode**: `1100011`  

---

12. **`bltz a0, 102e4 <__umoddi3+0x30>`**  
    - Opcode (B-Type): `1100011`  
    - Registers: `rs1 = a0 (x10)`, `rs2 = x0`  
    - Offset: `102e4 (calculated as a 12-bit signed offset)`  
    - Breakdown:  
      - **imm[12]**: `1`  
      - **imm[10:5]**: `100010`  
      - **rs2 (x0)**: `00000`  
      - **rs1 (a0)**: `01010`  
      - **funct3**: `100`  
      - **imm[4:1]**: `1110`  
      - **imm[11]**: `0`  
      - **opcode**: `1100011`  

---

13. **`auipc a5, 0xffff0`**  
    - Opcode (U-Type): `0010111`  
    - Register: `rd = a5 (x15)`  
    - Immediate: `0xffff0`  
    - Breakdown:  
      - **imm[31:12]**: `1111111111110000`  
      - **rd (a5)**: `01111`  
      - **opcode**: `0010111`  

---

14. **`j 10344 <atexit>`**  
    - Opcode (J-Type): `1101111`  
    - Register: `rd = x0` (unconditional jump)  
    - Offset: `10344 (calculated relative offset, 21 bits)`  
    - Breakdown:  
      - **imm[20]**: `1`  
      - **imm[10:1]**: `1001001100`  
      - **imm[11]**: `0`  
      - **imm[19:12]**: `0100000100`  
      - **rd (x0)**: `00000`  
      - **opcode**: `1101111`  

---

15. **`lw a0, 0(sp)`**  
    - Opcode (I-Type): `0000011`  
    - Registers: `rd = a0 (x10)`, `rs1 = sp (x2)`  
    - Immediate: `0`  
    - Breakdown:  
      - **imm[11:0]**: `000000000000`  
      - **rs1 (sp)**: `00010`  
      - **funct3**: `010`  
      - **rd (a0)**: `01010`  
      - **opcode**: `0000011`  

