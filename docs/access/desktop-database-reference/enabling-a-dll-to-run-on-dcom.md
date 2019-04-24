---
title: Como habilitar uma DLL para ser executada em DCOM
TOCTitle: Enabling a DLL to run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b97f4e8050cf293621c7b7fc79437c89171d86fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293543"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a>Como habilitar uma DLL para ser executada em DCOM


**Aplica-se ao:** Access 2013, Office 2013

As etapas a seguir descrevem como habilitar uma biblioteca de vínculo dinâmico do objeto de negócios para usar o DCOM e os serviços de informações da Internet (HTTP) via serviços de componente.

1.  Crie um novo pacote vazio no snap-in MMC dos Serviços de Componente. Você usará o snap-in MMC dos Serviços de Componente para criar um pacote e adicionar a DLL neste pacote. Isso faz com que a .dll seja acessível pelo DCOM, mas remove a acessibilidade pelo IIS. (Se você procurar no Registro por .dll, a chave **Inproc** agora estará vazia; a configuração do atributo Activation, explicado posteriormente neste capítulo, agrega um valor à chave **Inproc**.)

2.  Instale um objeto de negócios no pacote. -ou- Importe o objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) no pacote.

3.  Defina o atributo Activation para o pacote como **No processo do criador** (aplicativo Library). Para tornar a .dll acessível pelo DCOM e IIS no mesmo computador, você deve definir o atributo Activation do componente no snap-in MMC dos Serviços de Componente. Depois de definir o atributo como **No processo do criador**, você notará que uma chave do servidor **Inproc** no Registro foi adicionada, apontando para a .dll substituta dos Serviços de Componente.

