	Es una técnica para comunicar componentes, sean estos piezas de software 
	de un mismo sistema, o sistemas propiamente tal.

Cuando uno traspasa mensajes entre piezas de software o sistemas, puede realizarse mediante diferentes maneras, una de estas maneras corresponde a el protocolo [[MQTT (Message Queuing Telemetry Transport)]]. Este utiliza [[Mensajes|mensajes]] como elemento fundamental para comunicar estos mismos.

Los mensajes son representados en notación [[JSON (Javascript Object Notation)]]

![[Server.png]]

En la presente imagen, casa componente es un sistema independiente que funciona de manera asíncrona uno del otro, y no conoce quién es el receptor de la información enviada, dígase, desacoplados uno del otro.