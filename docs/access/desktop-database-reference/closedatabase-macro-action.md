---
title: Ação de macro FecharBancoDeDados
TOCTitle: CloseDatabase Macro Action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2c60d53b6798d3385bdcfb17669134a04ba6195
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465286"
---
# <a name="closedatabase-macro-action"></a><span data-ttu-id="0a878-102">Ação de macro FecharBancoDeDados</span><span class="sxs-lookup"><span data-stu-id="0a878-102">CloseDatabase Macro Action</span></span>


<span data-ttu-id="0a878-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a878-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0a878-104">Você pode usar a ação **FecharBancoDeDados** para fechar o banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="0a878-104">You can use the **CloseDatabase** action to close the current database.</span></span>

## <a name="setting"></a><span data-ttu-id="0a878-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="0a878-105">Setting</span></span>

<span data-ttu-id="0a878-106">A ação **FecharBancoDeDados** não tem nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="0a878-106">The **CloseDatabase** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a878-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a878-107">Remarks</span></span>

  - <span data-ttu-id="0a878-108">O Access não executará nenhuma ação que siga a ação **FecharBancoDeDados** em uma macro.</span><span class="sxs-lookup"><span data-stu-id="0a878-108">Access will not run any actions that follow the **CloseDatabase** action in a macro.</span></span>

  - <span data-ttu-id="0a878-109">Essa ação tem o mesmo efeito que clicar na guia **arquivo** e clicando em **Fechar do banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="0a878-109">This action has the same effect as clicking the **File** tab and then clicking **Close Database**.</span></span> <span data-ttu-id="0a878-110">Se houver algum objeto não salvo ao executar a ação **FecharBancoDeDados**, as caixas de diálogo exibidas serão as mesmas daquelas exibidas ao clicar em **Fechar Banco de Dados**.</span><span class="sxs-lookup"><span data-stu-id="0a878-110">If there are any unsaved objects open when you run the **CloseDatabase** action, the dialog boxes that appear are the same as those displayed when you click **Close Database**.</span></span>

  - <span data-ttu-id="0a878-111">Para executar a ação **FecharBancoDeDados** em um módulo do VBA (Visual Basic for Applications), use o método **CloseDatabase** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="0a878-111">To run the **CloseDatabase** action in a Visual Basic for Applications (VBA) module, use the **CloseDatabase** method of the **DoCmd** object.</span></span>

