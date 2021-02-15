---
title: Coleção Parameters (ADO)
TOCTitle: Parameters collection (ADO)
ms:assetid: 554387c3-3572-5391-3b24-c7d3443844cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249283(v=office.15)
ms:contentKeyID: 48544923
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231103
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: feb24e0f498e02bae01ef689a2ad62e487e314bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287941"
---
# <a name="parameters-collection-ado"></a><span data-ttu-id="d3e1b-102">Coleção Parameters (ADO)</span><span class="sxs-lookup"><span data-stu-id="d3e1b-102">Parameters collection (ADO)</span></span>


<span data-ttu-id="d3e1b-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3e1b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3e1b-104">Contém todos os objetos [Parameter](parameter-object-ado.md) de um objeto [Command](command-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d3e1b-104">Contains all the [Parameter](parameter-object-ado.md) objects of a [Command](command-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3e1b-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3e1b-105">Remarks</span></span>

<span data-ttu-id="d3e1b-106">Um objeto **Command** tem uma coleção **Parameters** composta de objetos **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="d3e1b-106">A **Command** object has a **Parameters** collection made up of **Parameter** objects.</span></span>

<span data-ttu-id="d3e1b-p101">O uso do método [Refresh](refresh-method-ado.md) em uma coleção **Parameters** do objeto **Command** recupera as informações de parâmetro do provedor para o procedimento armazenado ou a consulta parametrizada especificada no objeto **Command**. Alguns provedores não oferecem suporte às chamadas de procedimento armazenadas ou às consultas parametrizadas; a chamada do método **Refresh** na coleção **Parameters** durante o uso desse provedor retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="d3e1b-p101">Using the [Refresh](refresh-method-ado.md) method on a **Command** object's **Parameters** collection retrieves provider parameter information for the stored procedure or parameterized query specified in the **Command** object. Some providers do not support stored procedure calls or parameterized queries; calling the **Refresh** method on the **Parameters** collection when using such a provider will return an error.</span></span>

<span data-ttu-id="d3e1b-109">Se você não definiu seus próprios objetos **Parameter** e acessou a coleção **Parameters** antes de chamar o método **Refresh**, o ADO chamará automaticamente o método e preencherá a coleção.</span><span class="sxs-lookup"><span data-stu-id="d3e1b-109">If you have not defined your own **Parameter** objects and you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>

<span data-ttu-id="d3e1b-p102">Você pode minimizar as chamadas do provedor para melhorar o desempenho, se conhecer as propriedades dos parâmetros associadas ao procedimento armazenado ou à consulta parametrizada que quiser chamar. Use o método [CreateParameter](createparameter-method-ado.md) para criar objetos **Parameter** com as definições de propriedade adequadas e utilize o método [Append](append-method-ado.md) para adicioná-las à coleção **Parameters**. Isso permite definir e retornar os valores de parâmetro sem ter de chamar o provedor para obter as informações do parâmetro. Se você estiver gravando para um provedor que não forneça as informações de parâmetro, deverá preencher manualmente a coleção **Parameters** por meio desse método para usar os parâmetros totalmente. Use o método [Delete](delete-method-ado-parameters-collection.md) para remover os objetos **Parameter** da coleção **Parameters**, se necessário.</span><span class="sxs-lookup"><span data-stu-id="d3e1b-p102">You can minimize calls to the provider to improve performance if you know the properties of the parameters associated with the stored procedure or parameterized query you wish to call. Use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the [Append](append-method-ado.md) method to add them to the **Parameters** collection. This lets you set and return parameter values without having to call the provider for the parameter information. If you are writing to a provider that does not supply parameter information, you must manually populate the **Parameters** collection using this method to be able to use parameters at all. Use the [Delete](delete-method-ado-parameters-collection.md) method to remove **Parameter** objects from the **Parameters** collection if necessary.</span></span>

<span data-ttu-id="d3e1b-115">Os objetos da coleção **Parameters** de um **Recordset** sairão do escopo (e, por esse motivo, se tornarão não disponíveis), quando **Recordset** for fechado.</span><span class="sxs-lookup"><span data-stu-id="d3e1b-115">The objects in the **Parameters** collection of a **Recordset** go out of scope (therefore becoming unavailable) when the **Recordset** is closed.</span></span>

