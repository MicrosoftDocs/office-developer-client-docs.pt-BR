---
title: Ação da macro ExcluirRegistro
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8fb20068052972696b09ea0d2165b344e97ea922
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294012"
---
# <a name="deleterecord-macro-action"></a><span data-ttu-id="35b8d-102">Ação da macro ExcluirRegistro</span><span class="sxs-lookup"><span data-stu-id="35b8d-102">DeleteRecord macro action</span></span>

<span data-ttu-id="35b8d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="35b8d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="35b8d-104">Você pode usar a ação **ExcluirRegistro** para excluir um registro.</span><span class="sxs-lookup"><span data-stu-id="35b8d-104">You can use the **DeleteRecord** action to delete a record.</span></span>

## <a name="setting"></a><span data-ttu-id="35b8d-105">Setting</span><span class="sxs-lookup"><span data-stu-id="35b8d-105">Setting</span></span>

<span data-ttu-id="35b8d-106">O bloco de dados **ExcluirRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="35b8d-106">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35b8d-107">Argumento</span><span class="sxs-lookup"><span data-stu-id="35b8d-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="35b8d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="35b8d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35b8d-109"><strong>Alias de Registro</strong></span><span class="sxs-lookup"><span data-stu-id="35b8d-109"><strong>Record Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="35b8d-110">Uma cadeia de caracteres que identifica o registro a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="35b8d-110">A string that identifies the record to delete.</span></span> <span data-ttu-id="35b8d-111">Se o argumento <em>Alias</em> não for especificado, o registro atual será excluído.</span><span class="sxs-lookup"><span data-stu-id="35b8d-111">If the <em>Alias</em> argument is not specified, then the current record is deleted.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="35b8d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="35b8d-112">Remarks</span></span>

<span data-ttu-id="35b8d-113">Você pode usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o último registro criado em um bloco de dados **CriarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="35b8d-113">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="35b8d-114">Por exemplo, use a sintaxe a seguir para se referir ao registro criado mais recentemente:</span><span class="sxs-lookup"><span data-stu-id="35b8d-114">For example, use the following syntax to refer to the most recently created record:</span></span>

`[LastCreateRecordIdentity]`

