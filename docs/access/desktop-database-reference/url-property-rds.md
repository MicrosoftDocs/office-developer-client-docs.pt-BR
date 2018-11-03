---
title: Propriedade URL (RDS - referência de banco de dados da área de trabalho do Access)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f75e5e1a6d4df21970eea387ecd85ac8ef346a70
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943770"
---
# <a name="url-property-rds"></a><span data-ttu-id="67ad8-102">Propriedade URL (RDS)</span><span class="sxs-lookup"><span data-stu-id="67ad8-102">URL property (RDS)</span></span>


<span data-ttu-id="67ad8-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="67ad8-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="67ad8-104">Indica um cadeia de caracteres que contém uma URL relativa ou absoluta.</span><span class="sxs-lookup"><span data-stu-id="67ad8-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="67ad8-105">Você pode definir a propriedade **URL** no tempo de design na marca OBJECT do objeto [DataControl](datacontrol-object-rds.md) ou em tempo de execução no código de script.</span><span class="sxs-lookup"><span data-stu-id="67ad8-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ad8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67ad8-106">Syntax</span></span>

<span data-ttu-id="67ad8-107">Tempo de design: \<PARAM nome = valor "URL" = "Server"\></span><span class="sxs-lookup"><span data-stu-id="67ad8-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="67ad8-108">Tempo de execução: DataControl.URL="Server"</span><span class="sxs-lookup"><span data-stu-id="67ad8-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="67ad8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67ad8-109">Parameters</span></span>

- <span data-ttu-id="67ad8-110">*Server*</span><span class="sxs-lookup"><span data-stu-id="67ad8-110">*Server*</span></span>

  - <span data-ttu-id="67ad8-111">Um valor **String** que contém uma URL válida.</span><span class="sxs-lookup"><span data-stu-id="67ad8-111">A **String** value that contains a valid URL.</span></span>

- <span data-ttu-id="67ad8-112">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="67ad8-112">*DataControl*</span></span>

  - <span data-ttu-id="67ad8-113">Uma variável de objeto que representa um objeto **DataControl**.</span><span class="sxs-lookup"><span data-stu-id="67ad8-113">An object variable that represents a **DataControl** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="67ad8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="67ad8-114">Remarks</span></span>

<span data-ttu-id="67ad8-p101">Normalmente, a URL identifica um arquivo Active Server Page (.asp) que pode gerar e retornar um [Recordset](recordset-object-ado.md). Portanto, o usuário pode obter um **Recordset** sem ter que invocar o objeto [DataFactory](datafactory-object-rdsserver.md) do servidor ou programar um objeto comercial personalizado.</span><span class="sxs-lookup"><span data-stu-id="67ad8-p101">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md). Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="67ad8-117">Se a propriedade **URL** tiver sido definida, [SubmitChanges](submitchanges-method-rds.md) enviará as alterações para o local especificado pela URL.</span><span class="sxs-lookup"><span data-stu-id="67ad8-117">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>

