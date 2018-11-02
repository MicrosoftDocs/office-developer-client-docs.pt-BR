---
title: Propriedade Field2.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 10fed55e-c938-2ae6-8fd2-996745a63da3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845353(v=office.15)
ms:contentKeyID: 48543306
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101183
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 11f8d6bd01d1cbbf76dbbf45dbff4c50bf49fe59
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926469"
---
# <a name="field2originalvalue-property-dao"></a><span data-ttu-id="b778f-102">Propriedade Field2.OriginalValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="b778f-102">Field2.OriginalValue property (DAO)</span></span>


<span data-ttu-id="b778f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b778f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="b778f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b778f-104">Syntax</span></span>

<span data-ttu-id="b778f-105">*expressão* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="b778f-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="b778f-106">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="b778f-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b778f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b778f-107">Remarks</span></span>

<span data-ttu-id="b778f-p101">Durante uma atualização em lote otimista, pode ocorrer uma colisão em que um segundo cliente modifica o mesmo campo e registro enquanto o primeiro cliente recupera os dados e tenta fazer a atualização. A propriedade **OriginalValue** contém o valor do campo no momento em que o último **Update** em lote começa. Se esse valor não corresponder ao valor que está realmente no banco de dados quando o **Update** em lote tenta gravar no banco de dados, ocorrerá uma colisão. Quando isso ocorrer, o novo valor no banco de dados será acessível pela propriedade **VisibleValue**.</span><span class="sxs-lookup"><span data-stu-id="b778f-p101">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt. The **OriginalValue** property contains the value of the field at the time the last batch **Update** began. If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs. When this happens, the new value in the database will be accessible through the **VisibleValue** property.</span></span>

