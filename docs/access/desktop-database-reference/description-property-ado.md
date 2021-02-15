---
title: Propriedade Description (ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba6d05aa1bfb626520af60a30279983bae6fa566
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293928"
---
# <a name="description-property-ado"></a><span data-ttu-id="39f32-102">Propriedade Description (ADO)</span><span class="sxs-lookup"><span data-stu-id="39f32-102">Description property (ADO)</span></span>


<span data-ttu-id="39f32-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39f32-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39f32-104">Descreve um objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="39f32-104">Describes an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="39f32-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="39f32-105">Return value</span></span>

<span data-ttu-id="39f32-106">Retorna um valor **String** contendo uma descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="39f32-106">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="39f32-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="39f32-107">Remarks</span></span>

<span data-ttu-id="39f32-p101">Use a propriedade **Description** para obter uma breve descrição do erro. Exiba essa propriedade para alertar o usuário sobre um erro que você não pode ou não deseja resolver. A sequência virá do ADO ou de um provedor.</span><span class="sxs-lookup"><span data-stu-id="39f32-p101">Use the **Description** property to obtain a short description of the error. Display this property to alert the user to an error that you cannot or do not want to handle. The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="39f32-p102">Os provedores são responsáveis por passar textos de erro específicos para o ADO. O ADO adiciona um objeto [Error](error-object-ado.md) à coleção **Errors** a cada erro de provedor ou alerta que recebe. Enumere a coleção **Errors** para rastrear os erros que são passados pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="39f32-p102">Providers are responsible for passing specific error text to ADO. ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives. Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>

