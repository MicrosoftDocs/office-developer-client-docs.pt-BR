---
title: Propriedade Field.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 824c483f56f7b8cf4a5f09022cc3ca80101fc7f9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463347"
---
# <a name="fieldoriginalvalue-property-dao"></a><span data-ttu-id="1559e-102">Propriedade Field.OriginalValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="1559e-102">Field.OriginalValue Property (DAO)</span></span>


<span data-ttu-id="1559e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1559e-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="1559e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1559e-104">Syntax</span></span>

<span data-ttu-id="1559e-105">*expressão* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="1559e-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="1559e-106">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="1559e-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1559e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="1559e-107">Remarks</span></span>

<span data-ttu-id="1559e-p101">Durante uma atualização em lotes otimista, pode ocorrer uma colisão quando um segundo cliente modificar o mesmo campo e registro no intervalo entre a recuperação de dados e a tentativa de atualização do primeiro cliente. A propriedade **OriginalValue** contém o valor do campo na hora em que começou a última **Update** em lotes. Se esse valor não corresponder ao valor verdadeiro do banco de dados quando **Update** tentar fazer gravações no banco de dados, ocorrerá uma colisão. Quando isso acontecer, o novo valor do banco de dados será acessível por meio da propriedade **[VisibleValue](field-visiblevalue-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="1559e-p101">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt. The **OriginalValue** property contains the value of the field at the time the last batch **Update** began. If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs. When this happens, the new value in the database will be accessible through the **[VisibleValue](field-visiblevalue-property-dao.md)** property.</span></span>

