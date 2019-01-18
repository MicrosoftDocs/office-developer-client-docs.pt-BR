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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715778"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a><span data-ttu-id="7d5f2-102">Como habilitar uma DLL para ser executada em DCOM</span><span class="sxs-lookup"><span data-stu-id="7d5f2-102">Enabling a DLL to run on DCOM</span></span>


<span data-ttu-id="7d5f2-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d5f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7d5f2-104">As seguintes etapas descrevem como habilitar um bibliotecas de vínculos dinâmicos do objeto de negócios usar o DCOM e o Microsoft Internet Information Services (HTTP) pelos serviços de componente.</span><span class="sxs-lookup"><span data-stu-id="7d5f2-104">The following steps outline how to enable a business object dynamic-link libraries to use both DCOM and Microsoft Internet Information Services (HTTP) via Component Services.</span></span>

1.  <span data-ttu-id="7d5f2-p101">Crie um novo pacote vazio no snap-in MMC dos Serviços de Componente. Você usará o snap-in MMC dos Serviços de Componente para criar um pacote e adicionar a DLL neste pacote. Isso faz com que a .dll seja acessível pelo DCOM, mas remove a acessibilidade pelo IIS. (Se você procurar no Registro por .dll, a chave **Inproc** agora estará vazia; a configuração do atributo Activation, explicado posteriormente neste capítulo, agrega um valor à chave **Inproc**.)</span><span class="sxs-lookup"><span data-stu-id="7d5f2-p101">Create a new empty package in the Component Services MMC snap-in. You will use the Component Services MMC snap-in to create a package and add the DLL into this package. This makes the .dll accessible through DCOM, but it removes the accessibility through IIS. (If you check in the registry for the .dll, the **Inproc** key is now empty; setting the Activation attribute, explained later in this topic, adds a value in the **Inproc** key.)</span></span>

2.  <span data-ttu-id="7d5f2-p102">Instale um objeto de negócios no pacote. -ou- Importe o objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) no pacote.</span><span class="sxs-lookup"><span data-stu-id="7d5f2-p102">Install a business object into the package. -or- Import the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object into the package.</span></span>

3.  <span data-ttu-id="7d5f2-p103">Defina o atributo Activation para o pacote como **No processo do criador** (aplicativo Library). Para tornar a .dll acessível pelo DCOM e IIS no mesmo computador, você deve definir o atributo Activation do componente no snap-in MMC dos Serviços de Componente. Depois de definir o atributo como **No processo do criador**, você notará que uma chave do servidor **Inproc** no Registro foi adicionada, apontando para a .dll substituta dos Serviços de Componente.</span><span class="sxs-lookup"><span data-stu-id="7d5f2-p103">Set the Activation attribute for the package to **In the creator's process** (Library application). To make the .dll accessible through DCOM and IIS on the same computer, you must set the component's Activation attribute in the Component Services MMC snap-in. After you set the attribute to **In the creator's process**, you will notice that an **Inproc** server key in the registry has been added that points to a Component Services surrogate .dll.</span></span>

