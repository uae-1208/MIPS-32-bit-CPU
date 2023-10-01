transcript on
if ![file isdirectory verilog_libs] {
	file mkdir verilog_libs
}

vlib verilog_libs/altera_ver
vmap altera_ver ./verilog_libs/altera_ver
vlog -vlog01compat -work altera_ver {d:/altera/quartus ii 13.1/quartus/eda/sim_lib/altera_primitives.v}

vlib verilog_libs/lpm_ver
vmap lpm_ver ./verilog_libs/lpm_ver
vlog -vlog01compat -work lpm_ver {d:/altera/quartus ii 13.1/quartus/eda/sim_lib/220model.v}

vlib verilog_libs/sgate_ver
vmap sgate_ver ./verilog_libs/sgate_ver
vlog -vlog01compat -work sgate_ver {d:/altera/quartus ii 13.1/quartus/eda/sim_lib/sgate.v}

vlib verilog_libs/altera_mf_ver
vmap altera_mf_ver ./verilog_libs/altera_mf_ver
vlog -vlog01compat -work altera_mf_ver {d:/altera/quartus ii 13.1/quartus/eda/sim_lib/altera_mf.v}

vlib verilog_libs/altera_lnsim_ver
vmap altera_lnsim_ver ./verilog_libs/altera_lnsim_ver
vlog -sv -work altera_lnsim_ver {d:/altera/quartus ii 13.1/quartus/eda/sim_lib/altera_lnsim.sv}

vlib verilog_libs/cycloneiv_hssi_ver
vmap cycloneiv_hssi_ver ./verilog_libs/cycloneiv_hssi_ver
vlog -vlog01compat -work cycloneiv_hssi_ver {d:/altera/quartus ii 13.1/quartus/eda/sim_lib/cycloneiv_hssi_atoms.v}

vlib verilog_libs/cycloneiv_pcie_hip_ver
vmap cycloneiv_pcie_hip_ver ./verilog_libs/cycloneiv_pcie_hip_ver
vlog -vlog01compat -work cycloneiv_pcie_hip_ver {d:/altera/quartus ii 13.1/quartus/eda/sim_lib/cycloneiv_pcie_hip_atoms.v}

vlib verilog_libs/cycloneiv_ver
vmap cycloneiv_ver ./verilog_libs/cycloneiv_ver
vlog -vlog01compat -work cycloneiv_ver {d:/altera/quartus ii 13.1/quartus/eda/sim_lib/cycloneiv_atoms.v}

if {[file exists rtl_work]} {
	vdel -lib rtl_work -all
}
vlib rtl_work
vmap work rtl_work

vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/RTL {C:/Users/uae/Desktop/CPU/RTL/top.v}
vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/RTL {C:/Users/uae/Desktop/CPU/RTL/regfile.v}
vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/RTL {C:/Users/uae/Desktop/CPU/RTL/PC.v}
vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/RTL {C:/Users/uae/Desktop/CPU/RTL/NPC.v}
vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/RTL {C:/Users/uae/Desktop/CPU/RTL/mux2x32.v}
vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/RTL {C:/Users/uae/Desktop/CPU/RTL/JOIN.v}
vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/RTL {C:/Users/uae/Desktop/CPU/RTL/ext18.v}
vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/RTL {C:/Users/uae/Desktop/CPU/RTL/ext16.v}
vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/RTL {C:/Users/uae/Desktop/CPU/RTL/ext5.v}
vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/RTL {C:/Users/uae/Desktop/CPU/RTL/decoder.v}
vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/RTL {C:/Users/uae/Desktop/CPU/RTL/cpu.v}
vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/RTL {C:/Users/uae/Desktop/CPU/RTL/alu.v}
vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/RTL {C:/Users/uae/Desktop/CPU/RTL/imem.v}
vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/RTL {C:/Users/uae/Desktop/CPU/RTL/dmem.v}

vlog -vlog01compat -work work +incdir+C:/Users/uae/Desktop/CPU/Project/../TestBench {C:/Users/uae/Desktop/CPU/Project/../TestBench/top_tb.v}

vsim -t 1ps -L altera_ver -L lpm_ver -L sgate_ver -L altera_mf_ver -L altera_lnsim_ver -L cycloneiv_hssi_ver -L cycloneiv_pcie_hip_ver -L cycloneiv_ver -L rtl_work -L work -voptargs="+acc"  top_tb

add wave *
view structure
view signals
run 1 us
