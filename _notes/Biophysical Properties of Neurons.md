#06/15/23
## Passive properties

1.  Discuss the passive properties of dendrites  
	- membrane resistivity/conductance ($R_m/g_m$) -- input impedance/resistance / leak current
		- excitability of the neuron: $R_{in} = \frac{\Delta V}{\Delta I}$
		- $R_{in} = \frac{R_m}{4\pi a^2}$
		- https://www.youtube.com/watch?v=jxuwFG8C86U
		- https://zhuanlan.zhihu.com/p/93747037
	- membrane capacitance ($C_m$)
		- $C_{in} = C_m*(4\pi a^2)$  
		- $\Delta V = \Delta I*R_{in}(1-e^{-\frac{t}{\tau}}), \tau = R_{in}C_{in}$
		- When the capacitance of the cell membrane is *increased*, neurons become *less excitable* — that is, less likely to fire an action potential in response to input from other cells
			- $C_m$↑, $\tau$↑, $1-e^{-\frac{t}{\tau}}$↓, $\Delta V$↑
			
			![[Pasted image 20230616110028.png]] ![[Pasted image 20230616155933.png]]
	-  intracellular resistivity/conductance ($R_i/g_i$) ![[Pasted image 20230616110236.png]]
	- How do they influence synaptic integration depending on the distance a synapse has from the soma![[Pasted image 20230613183508.png]]
		- attenuation:  the impact of individual synapses on the generation of the neuronal output (axonal AP) is weak because of the biophysical constraints imposed by the morphology and membrane properties of the dendritic tree ![[#^37b30e]]
2.  Explain what electrotonic distance is
	- The electrotonic distance X is defined as X = x / lambda, where x is the physical distance along a cable, and lambda is the space constant (p. 76). Think of it as distance "in units of lambda"
	- In general(*infinite cylinder*), the steady-state space constant (sometimes called length constant) lambda is defined as $\lambda = \sqrt{\frac{rR_m}{2R_i}}$, where $r$ is the radius of the cylinder, $R_m$ is the specific membrane resistance, and $R_i$ is the specific intracellular (axial) resistivity (p. 64). In a cable with sealed ends, steady-state voltage will have decayed to values that are greater than 1/e at lambda (i.e. less attenuation), while it will have decayed to values that are smaller than 1/e in a cable with open ends
	- https://www.neuron.yale.edu/phpBB/viewtopic.php?t=1051#:~:text=The%20electrotonic%20distance%20X%20is,%22in%20units%20of%20lambda%22.

3.  How do inhibitory synapses influence excitatory synaptic transmission
	- inhibitory inputs do not simply counter the depolarizing effects of excitation, they are also critical determinants of spike timing
		- *synchronize* spiking in a population of neurons
			- cells receiving a common inhibitory input can stop spiking and subsequently return to threshold at the same time
		- limiting the *time window* for temporal summation of excitatory inputs
			- limit the *duration* of excitatory inputs to less than a few milliseconds
				- requiring *temporally coincident* excitatory inputs to trigger action potential firing
	- principles governing dendritic integration of EPSPs apply similarly to IPSPs
		- hyperpolarization by IPSPs will have *more effect* on the driving force for the inhibitory synaptic current for *synapses close together*
		- reversal potential at many inhibitory synapses is close to the resting membrane potential
			- little changes in $V_m$ (*no hyperpolarization*) can have relatively large effects on the inhibitory synaptic current (*shunting inhibition*)
				- the effect of the inhibitory conductance change is similar to a transient reduction in $R_m$ (*leak current*), which “shunts” the EPSP without an obvious change in membrane potential
				- https://www.youtube.com/watch?v=jB3sWyB8_WY
		- difference between membrane potential and EPSP
	- location-dependent effects
		- distal dendritic inhibition is only effective for excitatory synapses on the same dendritic branch as the inhibitory synapses (*on path*), and relatively ineffective if located on a dierent branch (*off path*)
		![[Pasted image 20230615183828.png]]![[Pasted image 20230615180314.png]]
	- effects on initiation and propagation of spikes in **active dendrites**
## Active properties

4.  Describe the properties of NMDA spikes and how they are generated
	- [generation of NMDA spikes](https://www.frontiersin.org/articles/10.3389/fnmol.2019.00238/full):
		- AMPA receptors in the spine mediate depolarization with fast decay, but that may promote the *release of $Mg^{2+}$ that blocks NMDA receptors (NMDARs)*
			- NMDARs are also glutamate receptors abundant in the dendritic spines and are highly permeable to $Ca^{2+}$ and $Na^+$, *mediating the majority of the postsynaptic $Ca^{2+}$  influx* during synaptic depolarization
				- NMDAR activation mediates a slow current that *persists for tens to hundreds of milliseconds*
					- As a result, synaptic inputs can, in certain conditions, trigger *regenerative dendritic events* that may be long-lasting, therefore also termed *“plateau potentials” or NMDA spikes*
		- ‘‘spike-chain’’ mechanism
			- the AMPA response evokes a fast local *sodium spikelet*, which elicits a slower calcium mediated regenerative response, which in turn initiates the full-blown NMDA spike
			- the activation of dendritic voltage-gated sodium channels is not the determining factor for the initiation of glutamate dependent dendritic spikes, sodium channels *assist* in spike initiation but are *not necessary* for it
		-  A key point is that at many dendritic locations it takes only *a small number of synaptic inputs* to evoke an NMDA spike: As few as ∼10 clustered single spine inputs may suffice
	- [location of NMDARs channel](https://onlinelibrary.wiley.com/doi/10.1002/jnr.22444): 
		- dominant depolarization-activated conductance in *thin (usually submicron-diameter) dendrites*![[Pasted image 20230619152811.png]] 
	- I-V relation for NMDAR:![[Pasted image 20230619161814.png]]
		- under conditions of abundant glutamate supply, the I-V relation of an NMDAR current has a waveform *similar* to the I-V relation of the voltage-gated $Na^+$ channel![[Pasted image 20230619162311.png]]
	- [amplitude and duration of NMDA spikes](https://onlinelibrary.wiley.com/doi/10.1002/jnr.22444):
		- the amplitude of the dendritic spike *does not* increase with further increase in stimulus intensity. This could be explained by the fact that the maximal amplitude of the NMDA dependent spike is determined by the glutamate reversal potential, which is about 0 mV
		- on the other hand, the duration of the dendritic plateau potential *grow linearly* with the stimulus intensity![[Pasted image 20230619182103.png]]
			- the thin dendritic branches have not lost the *ability to code the intensity of glutamatergic excitatory input*
				- all aspects of the ensuing dendritic plateau potentials (timing, amplitude, duration) are *mirrored* in the cell body
					- the dendritic I-O function becomes essentially the neuronal I-O profile, a flexible duration of dendritic plateau potentials is the basis for *linear correlation* between the intensity of glutamatergic stimulation received in the basilar dendrite and the number of somatic action potentials per stimulation event
	- [propagation of Dendritic NMDA spikes](https://onlinelibrary.wiley.com/doi/10.1002/jnr.22444):
		- calcium spikes and sodium APs: *global broadcasting* signals  
		- in contrast to them, the NMDA spikes in thin dendritic branches (basal, oblique, and tuft) can be *truly local and spatially restricted* phenomena involving only one sister branch in the entire dendritic tree
			- active dendrites of a single neuron can perform the *multiple independent subunit computations* and enrich the computational power and repertoire of cortical pyramidal cells
				- summation(a paper)
					- pattern of activation
				- drive calcium spike(apical trunk)
		- NMDA spikes can either be restricted to a branch, by failure of active propagation at the branchpoint (distal), or they can spread regeneratively to the soma to influence axonal output (proximal)
	- [importance of NMDA spikes](https://pubmed.ncbi.nlm.nih.gov/16181086/): 
		- different voltage- and ligand-gated ion channels located in the dendritic tree not only participate in processing afferent inputs, but also enable the dendritic tree to *initiate regenerative spikes*, traditionally considered to be exclusively restricted to axonal structures
			- *regenerative dendritic events* include spikes of activity that are generated within the dendrite itself or triggered by back-propagating action potentials.
			- these local dendritic spikes may act as a means to initiate *long-term synaptic plasticity*
				- different from *Hebbian synaptic plasticity*, this type of induction *does not need axonal action potential firing and backpropagation into the dendrite*
		- NMDA spikes depend on recent and ongoing activity in the local network and may serve as a powerful mechanism to modify the network by inducing the *long-term strengthening* of *co-activated* neighboring inputs
		- neurons capable of firing NMDA spikes can exhibit a *greater specificity of spiking responses* and perform a *greater number of transformations of synaptic input into an AP output*, which would otherwise require more than one neuron with passive dendrites  ^37b30e
		- *synchronization*
			- cortical Up states, via a massive increase in extracellular glutamate concentration, create favorable conditions for initiation of dendritic plateau potentials
				- in turn, dendritic NMDA spikes can bring cortical pyramidal neurons to a sustained depolarized state, the Up state
					- a transition from a Down state to an Up state dramatically *increases the AP firing probability* and therefore provides a *basis for synchronization* with an active assembly of neurons![[Pasted image 20230619192900.png]]
		- *temporal binding*: two features of dendritic glutamate-evoked plateau potentials may serve in the temporal binding processes of the CNS
			- maintenance of neuronal sustained depolarization, the Up state 
			- shortening of the neuronal membrane time constant
5.  Calcium spike
	- voltage-gated calcium channels allows apical dendrites to *propagate action potentials (AP) actively back into the dendritic tree* and to participate in *spike-timing-dependent synaptic plasticity (STDP)*
6.  Action potential backpropagation
7.  Compartment models![[Pasted image 20230616164449.png]]