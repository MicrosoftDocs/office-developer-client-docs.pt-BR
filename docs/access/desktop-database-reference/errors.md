---
title: Erros (referência do banco de dados de área de trabalho do Access)
TOCTitle: Errors
ms:assetid: 42f5cab9-f32a-d789-10e8-8d73892427f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249199(v=office.15)
ms:contentKeyID: 48544490
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 056ec0b34991348728898b4c0fc4a1a516a9913f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293354"
---
# <a name="errors"></a><span data-ttu-id="5c427-102">Erros</span><span class="sxs-lookup"><span data-stu-id="5c427-102">Errors</span></span>

<span data-ttu-id="5c427-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c427-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5c427-104">Qualquer operação envolvendo os objetos ADO pode gerar um ou vários erros de provedor.</span><span class="sxs-lookup"><span data-stu-id="5c427-104">Any operation involving ADO objects can generate one or more provider errors.</span></span> <span data-ttu-id="5c427-105">À medida que cada erro ocorrer, um ou vários objetos **Error** serão colocados na coleção **Errors** do objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="5c427-105">As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object.</span></span> <span data-ttu-id="5c427-106">Para obter detalhes sobre o tratamento de avisos e erros em seu aplicativo ADO, consulte o [capítulo 6: tratamento de erros](chapter-6-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="5c427-106">For details about handling warnings and errors in your ADO application, see [Chapter 6: Error handling](chapter-6-error-handling.md).</span></span>

<span data-ttu-id="5c427-p102">Um mecanismo individual pode gerar erros de aplicativo. Por exemplo, no Visual Basic, o objeto **Err** conterá os erros no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5c427-p102">Application errors can be raised by a separate mechanism. For example, in Visual Basic, the **Err** object will contain application-level errors.</span></span>

