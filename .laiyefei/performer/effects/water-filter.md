<div style="display: none">
	<svg width="0" height="0" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
		<filter id="water">
			<feTurbulence type="fractalNoise" baseFrequency=".05 .05" numOctaves="1" result="noise1"></feTurbulence>
			<feColorMatrix in="noise1" type="hueRotate" values="16.0949" result="noise2">
				<animate attributeName="values" from="0" to="360" dur="1s" repeatCount="indefinite">
				</animate>
			</feColorMatrix>
			<feDisplacementMap xChannelSelector="R" yChannelSelector="G" scale="7" in="SourceGraphic" in2="noise2">
			</feDisplacementMap>
		</filter>
	</svg>
	<!-- 
	add style do filter:
	 -o-object-fit: cover;
	     object-fit: cover;
	  -webkit-filter: url(#water);
	          filter: url(#water);
	 -->
	<link rel="stylesheet" type="text/css" href="{{ site.assets_dir }}/css/resos/water-filter.css" />
</div>