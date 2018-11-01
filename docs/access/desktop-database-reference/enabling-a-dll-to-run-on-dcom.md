---
title: Permitindo que uma DLL seja executada no DCOM
TOCTitle: Enabling a DLL to Run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 750848ce0e787506085899f4717730e1ca0a8f13
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868690"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a>Permitindo que uma DLL seja executada no DCOM


**Aplica-se a**: Access 2013, o Office 2013

As seguintes etapas destacam como ativar as bibliotecas de vínculos dinâmicos do objeto de negócios para usar o DCOM e o Microsoft® Internet Information Services (HTTP) pelos Serviços de Componente.

1.  Crie um novo pacote vazio no snap-in MMC dos Serviços de Componente. Você usará o snap-in MMC dos Serviços de Componente para criar um pacote e adicionar a DLL neste pacote. Isso faz com que a .dll seja acessível pelo DCOM, mas remove a acessibilidade pelo IIS. (Se você procurar no Registro por .dll, a chave **Inproc** agora estará vazia; a configuração do atributo Activation, explicado posteriormente neste capítulo, agrega um valor à chave **Inproc**.)

2.  Instale um objeto de negócios no pacote. -ou- Importe o objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) no pacote.

3.  Defina o atributo Activation para o pacote como **No processo do criador** (aplicativo Library). Para tornar a .dll acessível pelo DCOM e IIS no mesmo computador, você deve definir o atributo Activation do componente no snap-in MMC dos Serviços de Componente. Depois de definir o atributo como **No processo do criador**, você notará que uma chave do servidor **Inproc** no Registro foi adicionada, apontando para a .dll substituta dos Serviços de Componente.

