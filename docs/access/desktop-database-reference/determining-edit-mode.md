---
title: Determinando o modo de edição
TOCTitle: Determining Edit Mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 53167d7438ecce673fed64f3c7b8d53fbbfbaa5d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465273"
---
# <a name="determining-edit-mode"></a><span data-ttu-id="6fe09-102">Determinando o modo de edição</span><span class="sxs-lookup"><span data-stu-id="6fe09-102">Determining Edit Mode</span></span>


<span data-ttu-id="6fe09-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fe09-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6fe09-p101">O ADO mantém um buffer de edição associado ao registro atual. A propriedade **EditMode** indica se foram feitas alterações nesse buffer ou se um novo registro foi criado. Use **EditMode** para determinar o status de edição do registro atual. Você pode fazer um teste para saber se há alterações pendentes, caso um processo de edição tenha sido interrompido, e determinar se é necessário usar o método **Update** ou **CancelUpdate**.</span><span class="sxs-lookup"><span data-stu-id="6fe09-p101">ADO maintains an editing buffer associated with the current record. The **EditMode** property indicates whether changes have been made to this buffer or whether a new record has been created. Use **EditMode** to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the **Update** or **CancelUpdate** method.</span></span>

<span data-ttu-id="6fe09-108">**EditMode** retorna uma das constantes **EditModeEnum**, que são listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6fe09-108">**EditMode** returns one of the **EditModeEnum** constants, which are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6fe09-109">Constant</span><span class="sxs-lookup"><span data-stu-id="6fe09-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="6fe09-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fe09-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fe09-111"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="6fe09-111"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="6fe09-112">Indica que nenhuma operação de edição está em andamento.</span><span class="sxs-lookup"><span data-stu-id="6fe09-112">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fe09-113"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="6fe09-113"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="6fe09-114">Indica que os dados no registro atual foram modificados, mas não foram salvos.</span><span class="sxs-lookup"><span data-stu-id="6fe09-114">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fe09-115"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="6fe09-115"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="6fe09-116">Indica que o método <strong>AddNew</strong> foi chamado e que o registro atual no buffer de cópia é novo e não foi salvo no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6fe09-116">Indicates that the <strong>AddNew</strong> method has been called, and the current record in the copy buffer is a new record that has not been saved to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fe09-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="6fe09-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="6fe09-118">Indica que o registro atual foi excluído.</span><span class="sxs-lookup"><span data-stu-id="6fe09-118">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6fe09-p102">**EditMode** pode retornar um valor válido somente se houver um registro atual. **EditMode** retornará um erro se **BOF** ou **EOF** for **True** ou se o registro atual tiver sido excluído.</span><span class="sxs-lookup"><span data-stu-id="6fe09-p102">**EditMode** can return a valid value only if there is a current record. **EditMode** will return an error if **BOF** or **EOF** is **True** or if the current record has been deleted.</span></span>

