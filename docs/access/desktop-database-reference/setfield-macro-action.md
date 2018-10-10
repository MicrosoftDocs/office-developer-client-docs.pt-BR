---
title: Ação de macro DefinirCampo
TOCTitle: SetField Macro Action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7050065ccb42d5e6cc9347f32df056891f4ed078
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464272"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="815b4-102">Ação de macro DefinirCampo</span><span class="sxs-lookup"><span data-stu-id="815b4-102">SetField Macro Action</span></span>


<span data-ttu-id="815b4-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="815b4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="815b4-104">A ação **DefinirCampo** pode ser usada para atribuir um valor a um campo.</span><span class="sxs-lookup"><span data-stu-id="815b4-104">The **SetField** action can be used to assign a value to a field.</span></span>


> [!NOTE]
> <P><span data-ttu-id="815b4-105">[!OBSERVAçãO] A ação <STRONG>DefinirCampo</STRONG> está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="815b4-105">The <STRONG>SetField</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="815b4-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="815b4-106">Setting</span></span>

<span data-ttu-id="815b4-107">A ação **DefinirCampo** tem os seguintes listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="815b4-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="815b4-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="815b4-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="815b4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="815b4-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="815b4-110"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="815b4-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="815b4-111">Uma cadeia de caracteres que identifica o campo.</span><span class="sxs-lookup"><span data-stu-id="815b4-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="815b4-112"><strong>Valor</strong></span><span class="sxs-lookup"><span data-stu-id="815b4-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="815b4-113">Uma expressão que especifica o valor a ser atribuído ao campo.</span><span class="sxs-lookup"><span data-stu-id="815b4-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="815b4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="815b4-114">Remarks</span></span>

<span data-ttu-id="815b4-115">A ação **DefinirCampo** não pode ser usada fora de um bloco de dados **[CriarRegistro](createrecord-data-block.md)** ou **[EditarRegistro](editrecord-data-block.md)**.</span><span class="sxs-lookup"><span data-stu-id="815b4-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

