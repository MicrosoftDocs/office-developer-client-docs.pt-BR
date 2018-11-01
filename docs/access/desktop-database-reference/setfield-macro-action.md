---
title: Ação de macro DefinirCampo
TOCTitle: SetField Macro Action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1be405402c5f410c892c2dd8904133e09039351a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869498"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="2101b-102">Ação de macro DefinirCampo</span><span class="sxs-lookup"><span data-stu-id="2101b-102">SetField Macro Action</span></span>


<span data-ttu-id="2101b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="2101b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2101b-104">A ação **DefinirCampo** pode ser usada para atribuir um valor a um campo.</span><span class="sxs-lookup"><span data-stu-id="2101b-104">The **SetField** action can be used to assign a value to a field.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2101b-105">[!OBSERVAçãO] A ação <STRONG>DefinirCampo</STRONG> está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="2101b-105">The <STRONG>SetField</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="2101b-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="2101b-106">Setting</span></span>

<span data-ttu-id="2101b-107">A ação **DefinirCampo** tem os seguintes listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2101b-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2101b-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="2101b-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="2101b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2101b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2101b-110"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="2101b-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="2101b-111">Uma cadeia de caracteres que identifica o campo.</span><span class="sxs-lookup"><span data-stu-id="2101b-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2101b-112"><strong>Valor</strong></span><span class="sxs-lookup"><span data-stu-id="2101b-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="2101b-113">Uma expressão que especifica o valor a ser atribuído ao campo.</span><span class="sxs-lookup"><span data-stu-id="2101b-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2101b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2101b-114">Remarks</span></span>

<span data-ttu-id="2101b-115">A ação **DefinirCampo** não pode ser usada fora de um bloco de dados **[CriarRegistro](createrecord-data-block.md)** ou **[EditarRegistro](editrecord-data-block.md)**.</span><span class="sxs-lookup"><span data-stu-id="2101b-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

