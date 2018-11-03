---
title: O papel do ADO no Microsoft Data Access
TOCTitle: The Role of ADO in Microsoft Data Access
ms:assetid: e9087ec8-850b-ebbe-369a-a5987a528de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250180(v=office.15)
ms:contentKeyID: 48548433
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1675f674a07175b3cade82e5e5b43db29874bec2
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936718"
---
# <a name="the-role-of-ado-in-microsoft-data-access"></a><span data-ttu-id="a6efc-102">O papel do ADO no Microsoft Data Access</span><span class="sxs-lookup"><span data-stu-id="a6efc-102">The Role of ADO in Microsoft Data Access</span></span>

<span data-ttu-id="a6efc-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6efc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a6efc-p101">O Microsoft Data Access Components (MDAC) fornece acesso a dados independente de repositórios de dados, ferramentas e linguagens. Ele fornece uma interface fácil de usar de nível alto e uma interface de nível baixo e alto desempenho para praticamente qualquer repositório de dados disponível. Você pode usar essa flexibilidade para integrar vários repositórios de dados e usar suas opções de ferramentas, aplicativos e serviços de plataforma para criar as soluções certas para suas necessidades. Essa tecnologia fornece a moldura básica para o acesso a dados de uso geral nos sistemas operacionais Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a6efc-p101">The Microsoft Data Access Components (MDAC) provide data access that is independent of data stores, tools, and languages. It provides a high-level, easy-to-use interface, and a low-level, high-performance interface to practically any data store available. You can use this flexibility to integrate diverse data stores and use your choice of tools, applications, and platform services to create the right solutions for your needs. These technologies provide the basic framework for general-purpose data access in Microsoft Windows operating systems.</span></span>

<span data-ttu-id="a6efc-p102">Há três tecnologias principais no MDAC. O ActiveX Data Objects (ADO) é uma interface fácil de usar de nível alto para bancos de dados OLE. O banco de dados OLE é uma interface de nível baixo e alto desempenho para vários repositórios de dados. O ADO e o banco de dados OLE podem trabalhar com dados relacionais (tabulares) e não relacionais (hierárquicos ou de fluxo). Finalmente, o Open Database Connectivity (ODBC) é outra interface de baixo nível e alto desempenho criado especificamente para repositórios de dados relacionais.</span><span class="sxs-lookup"><span data-stu-id="a6efc-p102">There are three primary technologies in MDAC. ActiveX Data Objects (ADO) is a high-level, easy-to-use interface to OLE DB. OLE DB is a low-level, high-performance interface to a variety of data stores. ADO and OLE DB both can work with relational (tabular) and nonrelational (hierarchical or stream) data. Finally, Open Database Connectivity (ODBC) is another low-level, high-performance interface that is designed specifically for relational data stores.</span></span>

<span data-ttu-id="a6efc-p103">O ADO fornece uma camada de abstração entre seu aplicativo cliente ou da camada intermediária e as interfaces de banco de dados OLE de nível baixo. O ADO usa um pequeno conjunto de objetos Automation para fornecer uma interface simples e eficiente para o banco de dados OLE. Essa interface torna o ADO a opção perfeita para desenvolvedores em linguagens de níveis mais altos, como Visual Basic e até VBScript, que desejam acessar os dados sem precisar aprender as complexidades do COM e do banco de dados OLE.</span><span class="sxs-lookup"><span data-stu-id="a6efc-p103">ADO provides a layer of abstraction between your client or middle-tier application and the low-level OLE DB interfaces. ADO uses a small set of Automation objects to provide a simple and efficient interface to OLE DB. This interface makes ADO the perfect choice for developers in higher level languages, such as Visual Basic and even VBScript, who want to access data without having to learn the intricacies of COM and OLE DB.</span></span>

