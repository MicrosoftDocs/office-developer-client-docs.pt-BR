---
title: Propriedade Workspace. Type (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e698963d60809e8d88c4ff87532fb7b74cff275c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311302"
---
# <a name="workspacetype-property-dao"></a><span data-ttu-id="a89d6-102">Propriedade Workspace. Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="a89d6-102">Workspace.Type property (DAO)</span></span>


<span data-ttu-id="a89d6-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a89d6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a89d6-104">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto.</span><span class="sxs-lookup"><span data-stu-id="a89d6-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="a89d6-105">**Integer** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a89d6-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a89d6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a89d6-106">Syntax</span></span>

<span data-ttu-id="a89d6-107">*expressão* . Escreva</span><span class="sxs-lookup"><span data-stu-id="a89d6-107">*expression* .Type</span></span>

<span data-ttu-id="a89d6-108">*expressão* Uma variável que representa um objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="a89d6-108">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a89d6-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a89d6-109">Remarks</span></span>

<span data-ttu-id="a89d6-110">Para um objeto **Workspace**, as configurações e valores de retorno possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="a89d6-110">For a **Workspace** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a89d6-111">Constant</span><span class="sxs-lookup"><span data-stu-id="a89d6-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="a89d6-112">Tipo de Workspace</span><span class="sxs-lookup"><span data-stu-id="a89d6-112">Workspace type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a89d6-113"><strong>dbUseJet</strong></span><span class="sxs-lookup"><span data-stu-id="a89d6-113"><strong>dbUseJet</strong></span></span></p></td>
<td><p><span data-ttu-id="a89d6-114">O <strong>Workspace </strong> está conectado ao mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a89d6-114">The <strong>Workspace</strong> is connected to the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89d6-115"><strong>dbUseODBC</strong></span><span class="sxs-lookup"><span data-stu-id="a89d6-115"><strong>dbUseODBC</strong></span></span></p></td>
<td><p><span data-ttu-id="a89d6-116">O <strong>Workspace</strong> está conectado a uma fontes de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="a89d6-116">The <strong>Workspace</strong> is connected to an ODBC data source.</span></span></p></td>
</tr>
</tbody>
</table>

