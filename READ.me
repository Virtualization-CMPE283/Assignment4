CMPE-283 Virtualization Technologies Assignment-4
-------------------------------------------------------------------------- 
Team Members:
Gunjan Srivastava : gunjan.srivastava@sjsu.edu
Anupama Kurudi : anupama.kurudi@sjsu.edu
-------------------------------------------------------------------------- 
QUESTION 1: 

- Both Team Members installed and ran the setup on their respective systems.
-------------------------------------------------------------------------- 
Question 2:
Include a sample of your print of exit count output from dmesg from “with EPT” and “without EPT”.

Answer:
amak@anupama-kvm:~$ cpuid -l 0x4fffffff
CPU 0:
   0x4fffffff 0x00: eax=0x00501e70 ebx=0x00000006 ecx=0x553acc74 edx=0xffff9d40
CPU 1:
   0x4fffffff 0x00: eax=0x00501e77 ebx=0x00000006 ecx=0x553ba528 edx=0xffff9d40

(With ept=1)

[   83.178229] ***********DEBUG_BEGIN***********
[   83.178231] **** EAX: 1342177279
[   83.178232] **** (Total number of exits: 532866 EAX:= 532866
[   83.178233] **** ECX:= 0
[   83.178234] **** Exit_Reason : ALL , ExitCount : 532866
[   83.178234] ***********DEBUG_END***********


sudo insmod /lib/modules/5.10.0-rc2+/kernel/arch/x86/kvm/kvm-intel.ko ept=0

[   83.178229] ***********DEBUG_BEGIN***********
[   83.178231] **** EAX: 1342177279
[   83.178232] **** (Total number of exits: 532866 EAX:= 590142
[   83.178233] **** ECX:= 0
[   83.178234] **** Exit_Reason : ALL , ExitCount : 590142
[   83.178234] ***********DEBUG_END***********
-------------------------------------------------------------------------- 
Question 3:

What did you learn from the count of exits? Was the count what you expected? If not, why not?

Answer:

For assignment 4, we ran a minimal linux distribution on the virtual machine. This linux version only had a shell and no window manager.
The exit count for the current linux distribution after re-running the code in assignment 3 was "532866" with EPT enabled. This looks about right to us because the number of exits with the desktop manager loaded was about 9 million.

With EPT disabled though, KVM/QEMU was quite unstable. We weren't able to get the linux distribution to boot successfully and consistently. QEMU crashed most of the time during booting. Using dmesg we saw this message:

[  291.218811] BUG: kernel NULL pointer dereference, address: 00000000000000a4
[  291.218816] #PF: supervisor read access in kernel mode
[  291.218817] #PF: error_code(0x0000) - not-present page
[  291.218818] PGD 0 P4D 0
[  291.218822] Oops: 0000 [#1] SMP PTI
[  291.218824] CPU: 3 PID: 2355 Comm: CPU 0/KVM Not tainted 5.10.0-rc2+ #3
[  291.218825] Hardware name: VMware, Inc. VMware7,1/440BX Desktop Reference Platform, BIOS VMW71.00V.16221537.B64.2005150253 05/15/2020
[  291.218870] RIP: 0010:is_tdp_mmu_root+0x1c/0x40 [kvm]
[  291.218873] Code: f8 75 02 5d c3 0f 0b 5d c3 0f 1f 44 00 00 0f 1f 44 00 00 48 c1 ee 0c 55 48 c1 e6 06 48 03 35 0b 26 39 c9 48 8b 56 28 48 89 e5 <0f> b6 82 a4 00 00 00 84 c0 74 08 8b 42 50 85 c0 0f 95 c0 5d c3 66
[  291.218875] RSP: 0018:ffffbd6900ba3b40 EFLAGS: 00010286
[  291.218876] RAX: ffff971a5bc60388 RBX: 0000000000000000 RCX: 0000000000000000
[  291.218877] RDX: 0000000000000000 RSI: fffff2e8c0046000 RDI: ffffbd6901ca5000
[  291.218878] RBP: ffffbd6900ba3b40 R08: 0000000000000002 R09: 0000000000000000
[  291.218879] R10: 0000000000000000 R11: 0000000000000000 R12: 0000000000000014
[  291.218880] R13: 00000000000fe000 R14: 0000000000000000 R15: ffff971a5bc60000
[  291.218881] FS:  00007f83c5421700(0000) GS:ffff971b75ec0000(0000) knlGS:0000000000000000
[  291.218882] CS:  0010 DS: 0000 ES: 0000 CR0: 0000000080050033
[  291.218883] CR2: 00000000000000a4 CR3: 000000010f430002 CR4: 00000000001726e0
[  291.218906] Call Trace:
[  291.218929]  direct_page_fault+0x80/0x990 [kvm]
[  291.218935]  ? fix_rmode_seg+0xd0/0x370 [kvm_intel]
[  291.218948]  ? vmx_get_segment+0x6d/0x220 [kvm_intel]
[  291.218964]  nonpaging_page_fault+0x21/0x30 [kvm]
[  291.218978]  kvm_mmu_page_fault+0x34f/0x570 [kvm]
[  291.218992]  ? assign_eip_far.isra.0+0xee/0x210 [kvm]
[  291.219006]  ? writeback_registers+0x22/0x70 [kvm]
[  291.219009]  ? vmx_set_rflags+0xaa/0x240 [kvm_intel]
[  291.219025]  kvm_handle_page_fault+0xde/0x150 [kvm]
[  291.219040]  ? x86_emulate_instruction+0x5e3/0x7a0 [kvm]
[  291.219043]  handle_exception_nmi+0x5f1/0x860 [kvm_intel]
[  291.219047]  vmx_handle_exit_int+0x100/0x780 [kvm_intel]
[  291.219050]  vmx_handle_exit+0x34/0x40 [kvm_intel]
[  291.219065]  kvm_arch_vcpu_ioctl_run+0xd8c/0x18d0 [kvm]
[  291.219072]  ? fpu__restore_sig+0x2d/0x40
[  291.219092]  kvm_vcpu_ioctl+0x247/0x5f0 [kvm]
[  291.219098]  __x64_sys_ioctl+0x91/0xc0
[  291.219108]  do_syscall_64+0x38/0x90
[  291.219111]  entry_SYSCALL_64_after_hwframe+0x44/0xa9
[  291.219113] RIP: 0033:0x7f83c868950b

We even researched on google and found some articles from stack overflow and Ubuntu kernel mailing lists about patches applied to fix these errors. However, the mails and articles were older than 2017 and did not apply in the current context.

We were able to successfully get the linux second level VM to boot once. With EPT disabled, the exit count was "590142".
-------------------------------------------------------------------------- 
Question 4:
What changed between the two runs (ept vs no-ept)?

Answer:

The exit count with the EPT disabled was "590142", roughly about 10.75% higher. This can be attributed to all the exits that are encountered when memory access occurs and there is a page translation. It is clear that enabling EPT i.e. nested virtualization leads to faster execution times because of fewer VM exits.
