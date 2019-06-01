# Transient-VAWT
El software TRANSIENT VAWT implementa un algoritmo numérico para el cálculo de la etapa de arranque de aerogeneradores de eje vertical con álabes rectos de sección transversal con perfil alar. Este software permite el cálculo de las fuerzas aerodinámicas que actúan sobre el aerogenerador, teniendo en cuenta los parámetros geométricos principales que son el radio del rotor, la cuerda del perfil alar, la envergadura del ala y el número de álabes. También se tienen en cuenta los parámetros pertenecientes al fluido como son la densidad y la viscosidad absoluta. La interacción sólido fluido se incluye con el cálculo del número de Reynolds local para cada álabe y el ángulo de ataque que varía en función del ángulo de azimut del rotor y la razón de velocidad en la punta (Tip Speed Ratio en inglés).

% Import the data from Excel for a lookup table
data = xlsread('MySpreadsheet','Sheet1');
% Row indices for lookup table
breakpoints1 = data(2:end,1)';
% Column indices for lookup table
breakpoints2 = data(1,2:end);
% Output values for lookup table
table_data = data(2:end,2:end);
