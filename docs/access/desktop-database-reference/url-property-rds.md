---
title: Propriedade URL (RDS - referência de banco de dados da área de trabalho do Access)
TOCTitle: URL Property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4f179eb2c251ca96943a5f924b0ca51881aa371b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874157"
---
# <a name="url-property-rds"></a><span data-ttu-id="73f23-102">Propriedade URL (RDS)</span><span class="sxs-lookup"><span data-stu-id="73f23-102">URL Property (RDS)</span></span>


<span data-ttu-id="73f23-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="73f23-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="73f23-104">Indica um cadeia de caracteres que contém uma URL relativa ou absoluta.</span><span class="sxs-lookup"><span data-stu-id="73f23-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="73f23-105">Você pode definir a propriedade **URL** no tempo de design na marca OBJECT do objeto [DataControl](datacontrol-object-rds.md) ou em tempo de execução no código de script.</span><span class="sxs-lookup"><span data-stu-id="73f23-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="73f23-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73f23-106">Syntax</span></span>

<span data-ttu-id="73f23-107">Tempo de design: \<PARAM nome = valor "URL" = "Server"\></span><span class="sxs-lookup"><span data-stu-id="73f23-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="73f23-108">Tempo de execução: DataControl.URL="Server"</span><span class="sxs-lookup"><span data-stu-id="73f23-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="73f23-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73f23-109">Parameters</span></span>

  - <span data-ttu-id="73f23-110">*Server*</span><span class="sxs-lookup"><span data-stu-id="73f23-110">*Server*</span></span>

  - <span data-ttu-id="73f23-111">Um valor **String** que contém uma URL válida.</span><span class="sxs-lookup"><span data-stu-id="73f23-111">A **String** value that contains a valid URL.</span></span>

  - <span data-ttu-id="73f23-112">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="73f23-112">*DataControl*</span></span>

  - <span data-ttu-id="73f23-113">Uma variável de objeto que representa um objeto **DataControl**.</span><span class="sxs-lookup"><span data-stu-id="73f23-113">An object variable that represents a **DataControl** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="73f23-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="73f23-114">Remarks</span></span>

<span data-ttu-id="73f23-p101">Normalmente, a URL identifica um arquivo Active Server Page (.asp) que pode gerar e retornar um [Recordset](recordset-object-ado.md). Portanto, o usuário pode obter um **Recordset** sem ter que invocar o objeto [DataFactory](datafactory-object-rdsserver.md) do servidor ou programar um objeto comercial personalizado.</span><span class="sxs-lookup"><span data-stu-id="73f23-p101">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md). Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="73f23-117">Se a propriedade **URL** tiver sido definida, [SubmitChanges](submitchanges-method-rds.md) enviará as alterações para o local especificado pela URL.</span><span class="sxs-lookup"><span data-stu-id="73f23-117">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>

