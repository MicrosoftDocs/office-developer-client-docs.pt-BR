---
title: Permitindo que uma DLL seja executada no DCOM
TOCTitle: Enabling a DLL to Run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eeec1109d2e352d43eaaa66a7e081123d7f388ee
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937712"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a><span data-ttu-id="c4a2d-102">Permitindo que uma DLL seja executada no DCOM</span><span class="sxs-lookup"><span data-stu-id="c4a2d-102">Enabling a DLL to Run on DCOM</span></span>


<span data-ttu-id="c4a2d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4a2d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4a2d-104">As seguintes etapas descrevem como habilitar um bibliotecas de vínculos dinâmicos do objeto de negócios usar o DCOM e o Microsoft Internet Information Services (HTTP) pelos serviços de componente.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-104">The following steps outline how to enable a business object dynamic-link libraries to use both DCOM and Microsoft Internet Information Services (HTTP) via Component Services.</span></span>

1.  <span data-ttu-id="c4a2d-p101">Crie um novo pacote vazio no snap-in MMC dos Serviços de Componente. Você usará o snap-in MMC dos Serviços de Componente para criar um pacote e adicionar a DLL neste pacote. Isso faz com que a .dll seja acessível pelo DCOM, mas remove a acessibilidade pelo IIS. (Se você procurar no Registro por .dll, a chave **Inproc** agora estará vazia; a configuração do atributo Activation, explicado posteriormente neste capítulo, agrega um valor à chave **Inproc**.)</span><span class="sxs-lookup"><span data-stu-id="c4a2d-p101">Create a new empty package in the Component Services MMC snap-in. You will use the Component Services MMC snap-in to create a package and add the DLL into this package. This makes the .dll accessible through DCOM, but it removes the accessibility through IIS. (If you check in the registry for the .dll, the **Inproc** key is now empty; setting the Activation attribute, explained later in this topic, adds a value in the **Inproc** key.)</span></span>

2.  <span data-ttu-id="c4a2d-p102">Instale um objeto de negócios no pacote. -ou- Importe o objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) no pacote.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-p102">Install a business object into the package. -or- Import the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object into the package.</span></span>

3.  <span data-ttu-id="c4a2d-p103">Defina o atributo Activation para o pacote como **No processo do criador** (aplicativo Library). Para tornar a .dll acessível pelo DCOM e IIS no mesmo computador, você deve definir o atributo Activation do componente no snap-in MMC dos Serviços de Componente. Depois de definir o atributo como **No processo do criador**, você notará que uma chave do servidor **Inproc** no Registro foi adicionada, apontando para a .dll substituta dos Serviços de Componente.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-p103">Set the Activation attribute for the package to **In the creator's process** (Library application). To make the .dll accessible through DCOM and IIS on the same computer, you must set the component's Activation attribute in the Component Services MMC snap-in. After you set the attribute to **In the creator's process**, you will notice that an **Inproc** server key in the registry has been added that points to a Component Services surrogate .dll.</span></span>

