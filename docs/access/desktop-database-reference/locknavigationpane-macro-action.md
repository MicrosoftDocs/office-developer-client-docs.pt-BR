---
title: Ação de macro BloquearPainelDeNavegação
TOCTitle: LockNavigationPane Macro Action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2db34ee9ea56c5fcb4c5aff6afa57c3f59d1f17c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870328"
---
# <a name="locknavigationpane-macro-action"></a><span data-ttu-id="cebb8-102">Ação de macro BloquearPainelDeNavegação</span><span class="sxs-lookup"><span data-stu-id="cebb8-102">LockNavigationPane Macro Action</span></span>


<span data-ttu-id="cebb8-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="cebb8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cebb8-104">Você pode usar a ação **BloquearPainelDeNavegação** para impedir que os usuários excluam objetos de banco de dados exibidos no Painel de Navegação.</span><span class="sxs-lookup"><span data-stu-id="cebb8-104">You can use the **LockNavigationPane** action to prevent users from deleting database objects that are displayed in the Navigation Pane.</span></span>

## <a name="setting"></a><span data-ttu-id="cebb8-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="cebb8-105">Setting</span></span>

<span data-ttu-id="cebb8-106">A ação **BloquearPainelDeNavegação** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="cebb8-106">The **LockNavigationPane** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cebb8-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="cebb8-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="cebb8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="cebb8-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cebb8-109"><strong>Lock</strong></span><span class="sxs-lookup"><span data-stu-id="cebb8-109"><strong>Lock</strong></span></span></p></td>
<td><p><span data-ttu-id="cebb8-110">Selecione <strong>Sim</strong> para bloquear o Painel de Navegação ou <strong>Não</strong> para desbloqueá-lo.</span><span class="sxs-lookup"><span data-stu-id="cebb8-110">Select <strong>Yes</strong> to lock the Navigation Pane, or <strong>No</strong> to unlock the Navigation Pane.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cebb8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cebb8-111">Remarks</span></span>

<span data-ttu-id="cebb8-112">O bloqueio do Painel de Navegação impede que você exclua os objetos de banco de dados ou recorte-os para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="cebb8-112">Locking the Navigation Pane prevents you from deleting database objects or cutting database objects to the clipboard.</span></span> <span data-ttu-id="cebb8-113">Ela faz *não* impede que você realize qualquer uma das seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="cebb8-113">It does *not* prevent you from performing any of the following operations:</span></span>

  - <span data-ttu-id="cebb8-114">Copiar objetos de banco de dados para a área de transferência</span><span class="sxs-lookup"><span data-stu-id="cebb8-114">Copying database objects to the clipboard</span></span>

  - <span data-ttu-id="cebb8-115">Colar objetos de banco de dados da área de transferência</span><span class="sxs-lookup"><span data-stu-id="cebb8-115">Pasting database objects from the clipboard</span></span>

  - <span data-ttu-id="cebb8-116">Exibir ou ocultar o Painel de Navegação</span><span class="sxs-lookup"><span data-stu-id="cebb8-116">Displaying or hiding the Navigation Pane</span></span>

  - <span data-ttu-id="cebb8-117">Selecionar diferentes esquemas de organização do Painel de Navegação</span><span class="sxs-lookup"><span data-stu-id="cebb8-117">Selecting different Navigation Pane organization schemes</span></span>

  - <span data-ttu-id="cebb8-118">Mostrar ou ocultar seções do Painel de Navegação</span><span class="sxs-lookup"><span data-stu-id="cebb8-118">Showing or hiding sections of the Navigation Pane</span></span>

<span data-ttu-id="cebb8-119">Para executar a ação **BloquearPainelDeNavegação** em um módulo do VBA, use o método **LockNavigationPane** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="cebb8-119">To run the **LockNavigationPane** action in a VBA module, use the **LockNavigationPane** method of the **DoCmd** object.</span></span>

