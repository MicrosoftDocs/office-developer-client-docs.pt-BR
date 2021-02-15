---
title: Método Append (Tabelas do ADOX)
TOCTitle: Append method (ADOX Tables)
ms:assetid: 9e9fd57c-a856-6179-013f-9f378c3b7df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249726(v=office.15)
ms:contentKeyID: 48546664
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d2bf2479c2a34291f245783ebaecd75ba31d2ac8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297071"
---
# <a name="append-method-adox-tables"></a><span data-ttu-id="2605c-102">Método Append (Tabelas do ADOX)</span><span class="sxs-lookup"><span data-stu-id="2605c-102">Append method (ADOX Tables)</span></span>

<span data-ttu-id="2605c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2605c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2605c-104">Adiciona um novo objeto [Table](table-object-adox.md) à coleção [Tables](tables-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="2605c-104">Adds a new [Table](table-object-adox.md) object to the [Tables](tables-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2605c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2605c-105">Syntax</span></span>

<span data-ttu-id="2605c-106">*Tabelas*. Append *Table*</span><span class="sxs-lookup"><span data-stu-id="2605c-106">*Tables*.Append *Table*</span></span>

## <a name="parameters"></a><span data-ttu-id="2605c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2605c-107">Parameters</span></span>

|<span data-ttu-id="2605c-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="2605c-108">Parameter</span></span>|<span data-ttu-id="2605c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2605c-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2605c-110">*Table*</span><span class="sxs-lookup"><span data-stu-id="2605c-110">*Table*</span></span> | <span data-ttu-id="2605c-111">Um valor **Variant** que contém uma referência à **Tabela** a ser anexada ou ao nome da tabela a ser criada e anexada.</span><span class="sxs-lookup"><span data-stu-id="2605c-111">A **Variant** value that contains a reference to the **Table** to append or the name of the table to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2605c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2605c-112">Remarks</span></span>

<span data-ttu-id="2605c-113">Ocorrerá um erro se o provedor não oferecer suporte à criação de tabelas.</span><span class="sxs-lookup"><span data-stu-id="2605c-113">An error will occur if the provider does not support creating tables.</span></span>

