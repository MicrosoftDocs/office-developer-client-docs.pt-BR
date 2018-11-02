---
title: Ação da macro DefinirCampo
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d8ca2315a9a84000aa29b88043e4edea05ffb0ea
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922822"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="8aa2f-102">Ação da macro DefinirCampo</span><span class="sxs-lookup"><span data-stu-id="8aa2f-102">SetField macro action</span></span>


<span data-ttu-id="8aa2f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8aa2f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8aa2f-104">A ação **DefinirCampo** pode ser usada para atribuir um valor a um campo.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-104">The **SetField** action can be used to assign a value to a field.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8aa2f-105">[!OBSERVAçãO] A ação <STRONG>DefinirCampo</STRONG> está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-105">The <STRONG>SetField</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="8aa2f-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="8aa2f-106">Setting</span></span>

<span data-ttu-id="8aa2f-107">A ação **DefinirCampo** tem os seguintes listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8aa2f-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="8aa2f-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="8aa2f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8aa2f-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8aa2f-110"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="8aa2f-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="8aa2f-111">Uma cadeia de caracteres que identifica o campo.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8aa2f-112"><strong>Valor</strong></span><span class="sxs-lookup"><span data-stu-id="8aa2f-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="8aa2f-113">Uma expressão que especifica o valor a ser atribuído ao campo.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8aa2f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8aa2f-114">Remarks</span></span>

<span data-ttu-id="8aa2f-115">A ação **DefinirCampo** não pode ser usada fora de um bloco de dados **[CriarRegistro](createrecord-data-block.md)** ou **[EditarRegistro](editrecord-data-block.md)**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

