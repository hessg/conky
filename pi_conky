#!/bin/bash

ssh_key='~/.ssh/pi_conky'
raspi='conky@192.168.0.50'
outfile='~/.config/conky/pi_values_conky'
cpu='pi_cpu_conky'
temp='pi_temp_conky'
mem='pi_mem_conky'
swap='pi_swap_conky'

get_values()
{
	result=`ssh -i ${ssh_key} ${raspi} ${!1}`
	echo "$result"
}

while :
do
	_cpu=`get_values 'cpu'`
	_temp=`get_values 'temp'`
	_mem=`get_values 'mem'`
	_swap=`get_values 'swap'`
	_out="cpu\t$_cpu\n\rtemp\t$_temp\n\rmem\t$_mem\n\rswap\t$_swap"
	echo -e $_out > pi_values_conky
	sleep 4s
done
