---
title: Ação da macro BloquearPainelDeNavegação
TOCTitle: LockNavigationPane macro action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7f6ee19edaf2efdc03301e98e709db6dd69f101a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717801"
---
# <a name="locknavigationpane-macro-action"></a><span data-ttu-id="41067-102">Ação da macro BloquearPainelDeNavegação</span><span class="sxs-lookup"><span data-stu-id="41067-102">LockNavigationPane macro action</span></span>


<span data-ttu-id="41067-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="41067-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="41067-104">Você pode usar a ação **BloquearPainelDeNavegação** para impedir que os usuários excluam objetos de banco de dados exibidos no Painel de Navegação.</span><span class="sxs-lookup"><span data-stu-id="41067-104">You can use the **LockNavigationPane** action to prevent users from deleting database objects that are displayed in the Navigation Pane.</span></span>

## <a name="setting"></a><span data-ttu-id="41067-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="41067-105">Setting</span></span>

<span data-ttu-id="41067-106">A ação **BloquearPainelDeNavegação** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="41067-106">The **LockNavigationPane** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41067-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="41067-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="41067-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="41067-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41067-109"><strong>Lock</strong></span><span class="sxs-lookup"><span data-stu-id="41067-109"><strong>Lock</strong></span></span></p></td>
<td><p><span data-ttu-id="41067-110">Selecione <strong>Sim</strong> para bloquear o Painel de Navegação ou <strong>Não</strong> para desbloqueá-lo.</span><span class="sxs-lookup"><span data-stu-id="41067-110">Select <strong>Yes</strong> to lock the Navigation Pane, or <strong>No</strong> to unlock the Navigation Pane.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="41067-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="41067-111">Remarks</span></span>

<span data-ttu-id="41067-112">O bloqueio do Painel de Navegação impede que você exclua os objetos de banco de dados ou recorte-os para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="41067-112">Locking the Navigation Pane prevents you from deleting database objects or cutting database objects to the clipboard.</span></span> <span data-ttu-id="41067-113">Ela faz *não* impede que você realize qualquer uma das seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="41067-113">It does *not* prevent you from performing any of the following operations:</span></span>

  - <span data-ttu-id="41067-114">Copiar objetos de banco de dados para a área de transferência</span><span class="sxs-lookup"><span data-stu-id="41067-114">Copying database objects to the clipboard</span></span>

  - <span data-ttu-id="41067-115">Colar objetos de banco de dados da área de transferência</span><span class="sxs-lookup"><span data-stu-id="41067-115">Pasting database objects from the clipboard</span></span>

  - <span data-ttu-id="41067-116">Exibir ou ocultar o Painel de Navegação</span><span class="sxs-lookup"><span data-stu-id="41067-116">Displaying or hiding the Navigation Pane</span></span>

  - <span data-ttu-id="41067-117">Selecionar diferentes esquemas de organização do Painel de Navegação</span><span class="sxs-lookup"><span data-stu-id="41067-117">Selecting different Navigation Pane organization schemes</span></span>

  - <span data-ttu-id="41067-118">Mostrar ou ocultar seções do Painel de Navegação</span><span class="sxs-lookup"><span data-stu-id="41067-118">Showing or hiding sections of the Navigation Pane</span></span>

<span data-ttu-id="41067-119">Para executar a ação **BloquearPainelDeNavegação** em um módulo do VBA, use o método **LockNavigationPane** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="41067-119">To run the **LockNavigationPane** action in a VBA module, use the **LockNavigationPane** method of the **DoCmd** object.</span></span>

