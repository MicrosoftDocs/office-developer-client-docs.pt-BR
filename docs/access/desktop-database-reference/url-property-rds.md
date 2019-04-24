---
title: Propriedade URL (referência do banco de dados de área de trabalho do Access)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aafc8cc10410cafed21e38ad7fec269c391c1fa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313395"
---
# <a name="url-property-rds"></a><span data-ttu-id="be098-102">Propriedade URL (RDS)</span><span class="sxs-lookup"><span data-stu-id="be098-102">URL property (RDS)</span></span>

<span data-ttu-id="be098-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be098-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be098-104">Indica um cadeia de caracteres que contém uma URL relativa ou absoluta.</span><span class="sxs-lookup"><span data-stu-id="be098-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="be098-105">Você pode definir a propriedade **URL** no tempo de design na marca OBJECT do objeto [DataControl](datacontrol-object-rds.md) ou em tempo de execução no código de script.</span><span class="sxs-lookup"><span data-stu-id="be098-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="be098-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be098-106">Syntax</span></span>

<span data-ttu-id="be098-107">Tempo de design \<: parâmetro Name = "URL" value = "Server"\></span><span class="sxs-lookup"><span data-stu-id="be098-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="be098-108">Tempo de execução: dataControl. URL = "Server"</span><span class="sxs-lookup"><span data-stu-id="be098-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="be098-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be098-109">Parameters</span></span>

|<span data-ttu-id="be098-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="be098-110">Parameter</span></span>|<span data-ttu-id="be098-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="be098-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="be098-112">*Server*</span><span class="sxs-lookup"><span data-stu-id="be098-112">*Server*</span></span> |<span data-ttu-id="be098-113">Um valor **String** que contém uma URL válida.</span><span class="sxs-lookup"><span data-stu-id="be098-113">A **String** value that contains a valid URL.</span></span>|
|<span data-ttu-id="be098-114">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="be098-114">*DataControl*</span></span> |<span data-ttu-id="be098-115">Uma variável de objeto que representa um objeto **DataControl**.</span><span class="sxs-lookup"><span data-stu-id="be098-115">An object variable that represents a **DataControl** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="be098-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="be098-116">Remarks</span></span>

<span data-ttu-id="be098-p101">Normalmente, a URL identifica um arquivo Active Server Page (.asp) que pode gerar e retornar um [Recordset](recordset-object-ado.md). Portanto, o usuário pode obter um **Recordset** sem ter que invocar o objeto [DataFactory](datafactory-object-rdsserver.md) do servidor ou programar um objeto comercial personalizado.</span><span class="sxs-lookup"><span data-stu-id="be098-p101">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md). Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="be098-119">Se a propriedade **URL** tiver sido definida, [SubmitChanges](submitchanges-method-rds.md) enviará as alterações para o local especificado pela URL.</span><span class="sxs-lookup"><span data-stu-id="be098-119">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>

