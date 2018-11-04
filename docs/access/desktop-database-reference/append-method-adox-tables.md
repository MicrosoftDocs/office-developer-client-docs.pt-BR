---
title: Método Append (Tabelas do ADOX)
TOCTitle: Append method (ADOX Tables)
ms:assetid: 9e9fd57c-a856-6179-013f-9f378c3b7df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249726(v=office.15)
ms:contentKeyID: 48546664
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8e43f8fe5537ded015b5b8d79bb32f811e73368c
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949345"
---
# <a name="append-method-adox-tables"></a><span data-ttu-id="82ac5-102">Método Append (Tabelas do ADOX)</span><span class="sxs-lookup"><span data-stu-id="82ac5-102">Append method (ADOX Tables)</span></span>

<span data-ttu-id="82ac5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="82ac5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82ac5-104">Adiciona um novo objeto [Table](table-object-adox.md) à coleção [Tables](tables-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="82ac5-104">Adds a new [Table](table-object-adox.md) object to the [Tables](tables-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="82ac5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82ac5-105">Syntax</span></span>

<span data-ttu-id="82ac5-106">*Tabelas*. Acrescentar*tabela*</span><span class="sxs-lookup"><span data-stu-id="82ac5-106">*Tables*.Append*Table*</span></span>

## <a name="parameters"></a><span data-ttu-id="82ac5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82ac5-107">Parameters</span></span>

|<span data-ttu-id="82ac5-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="82ac5-108">Parameter</span></span>|<span data-ttu-id="82ac5-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="82ac5-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="82ac5-110">*Table*</span><span class="sxs-lookup"><span data-stu-id="82ac5-110">*Table*</span></span> | <span data-ttu-id="82ac5-111">Um valor **Variant** que contém uma referência à **Tabela** a ser anexada ou ao nome da tabela a ser criada e anexada.</span><span class="sxs-lookup"><span data-stu-id="82ac5-111">A **Variant** value that contains a reference to the **Table** to append or the name of the table to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="82ac5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="82ac5-112">Remarks</span></span>

<span data-ttu-id="82ac5-113">Ocorrerá um erro se o provedor não oferecer suporte à criação de tabelas.</span><span class="sxs-lookup"><span data-stu-id="82ac5-113">An error will occur if the provider does not support creating tables.</span></span>

