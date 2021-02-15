---
title: Método Refresh (RDS)
TOCTitle: Refresh method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 60de3b25e5eedc277eaafbe4bd1c078863e13f7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309294"
---
# <a name="refresh-method-rds"></a><span data-ttu-id="597b3-102">Método Refresh (RDS)</span><span class="sxs-lookup"><span data-stu-id="597b3-102">Refresh method (RDS)</span></span>

<span data-ttu-id="597b3-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="597b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="597b3-104">Consulta novamente a fonte de dados especificada na propriedade [Connect](connect-property-rds.md) e atualiza os resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="597b3-104">Requeries the data source specified in the [Connect](connect-property-rds.md) property and updates the query results.</span></span>

## <a name="syntax"></a><span data-ttu-id="597b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="597b3-105">Syntax</span></span>

<span data-ttu-id="597b3-106">*DataControl*. Atualizar</span><span class="sxs-lookup"><span data-stu-id="597b3-106">*DataControl*.Refresh</span></span>

## <a name="parameters"></a><span data-ttu-id="597b3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="597b3-107">Parameters</span></span>

|<span data-ttu-id="597b3-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="597b3-108">Parameter</span></span>|<span data-ttu-id="597b3-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="597b3-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="597b3-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="597b3-110">*DataControl*</span></span> |<span data-ttu-id="597b3-111">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="597b3-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="597b3-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="597b3-112">Remarks</span></span>

<span data-ttu-id="597b3-p101">Você deve definir as propriedades [Connect](connect-property-rds.md), [Server](server-property-rds.md) e [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) antes de utilizar o método **Refresh**. Todos os controles acoplados a dados no formulário associado a um objeto **RDS.DataControl** refletirão o novo conjunto de registros. Qualquer objeto [Recordset](recordset-object-ado.md) pré-existente será liberado e quaisquer alterações não salvas serão descartadas. O método **Refresh** torna automaticamente o primeiro registro o registro atual.</span><span class="sxs-lookup"><span data-stu-id="597b3-p101">You must set the [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) properties before you use the **Refresh** method. All data-bound controls on the form associated with an **RDS.DataControl** object will reflect the new set of records. Any pre-existing [Recordset](recordset-object-ado.md) object is released, and any unsaved changes are discarded. The **Refresh** method automatically makes the first record the current record.</span></span>

<span data-ttu-id="597b3-p102">É uma boa ideia chamar o método **Refresh** periodicamente ao trabalhar com dados. Se você recuperar dados e, em seguida, deixá-los na máquina cliente por um tempo, é provável que eles fiquem desatualizados. É possível que quaisquer alterações que você fez falhem, porque alguma outra pessoa pode ter alterado o registro e submetido alterações antes de você.</span><span class="sxs-lookup"><span data-stu-id="597b3-p102">It's a good idea to call the **Refresh** method periodically when you work with data. If you retrieve data, and then leave it on your client machine for a while, it is likely to become out of date. It's possible that any changes you make will fail, because someone else might have changed the record and submitted changes before you.</span></span>

