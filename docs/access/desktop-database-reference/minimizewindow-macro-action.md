---
title: Ação da macro MinimizarJanela
TOCTitle: MinimizeWindow macro action
ms:assetid: 3a92b654-15ce-1ed1-63e0-eed927dbe26c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192648(v=office.15)
ms:contentKeyID: 48544265
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm174420
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 50716a32d0fa3837f87d9d2c5ecde0b59696480d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920365"
---
# <a name="minimizewindow-macro-action"></a><span data-ttu-id="da3a6-102">Ação da macro MinimizarJanela</span><span class="sxs-lookup"><span data-stu-id="da3a6-102">MinimizeWindow macro action</span></span>


<span data-ttu-id="da3a6-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="da3a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="da3a6-104">Se o Access estiver configurado para usar janelas sobrepostas em vez de documentos com guias, você pode usar a ação **Minimizarjanela** para reduzir a janela ativa para uma barra de título pequena na parte inferior da janela do Access.</span><span class="sxs-lookup"><span data-stu-id="da3a6-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MinimizeWindow** action to reduce the active window to a small title bar at the bottom of the Access window.</span></span>


> [!NOTE]
> <P><span data-ttu-id="da3a6-p101">[!OBSERVAçãO] Esta ação não pode ser aplicada a janelas de código no Editor do Visual Basic (VBE). Para obter informações sobre como afetar janelas de código, consulte o tópico da propriedade <STRONG>WindowState</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="da3a6-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the <STRONG>WindowState</STRONG> property topic.</span></span></P>



## <a name="setting"></a><span data-ttu-id="da3a6-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="da3a6-107">Setting</span></span>

<span data-ttu-id="da3a6-108">A ação **MinimizarJanela** não tem nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="da3a6-108">The **MinimizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="da3a6-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="da3a6-109">Remarks</span></span>

<span data-ttu-id="da3a6-p102">Você pode usar esta ação para remover uma janela da tela enquanto deixa o objeto aberto. Também pode usar esta ação para abrir um objeto sem exibir sua janela. Para exibir o objeto, use a ação **SelecionarObjeto** com a ação **MaximizarJanela** ou **Restaurar**. A ação **RestaurarJanela** restaura uma janela minimizada para o tamanho anterior.</span><span class="sxs-lookup"><span data-stu-id="da3a6-p102">You can use this action to remove a window from the screen while leaving the object open. You can also use this action to open an object without displaying its window. To display the object, use the **SelectObject** action with either the **MaximizeWindow** or **RestoreWindow** action. The **RestoreWindow** action restores a minimized window to its previous size.</span></span>

<span data-ttu-id="da3a6-114">A ação **MinimizarJanela** equivale a clicar no botão **Minimizar** no canto superior direito da janela ou clicar em **Minimizar** no menu **Controle** da janela.</span><span class="sxs-lookup"><span data-stu-id="da3a6-114">The **MinimizeWindow** action has the same effect as clicking the **Minimize** button in the window's upper-right corner or clicking **Minimize** on the window's **Control** menu.</span></span>

<span data-ttu-id="da3a6-115">**Dicas**</span><span class="sxs-lookup"><span data-stu-id="da3a6-115">**Tips**</span></span>

  - <span data-ttu-id="da3a6-116">Talvez seja necessário primeiro usar a ação **SelecionarObjeto** se a janela a ser minimizada não for a janela ativa.</span><span class="sxs-lookup"><span data-stu-id="da3a6-116">You may first need to use the **SelectObject** action if the window you want to minimize isn't the active window.</span></span>

  - <span data-ttu-id="da3a6-p103">Para ocultar o Painel de Navegação, use a ação **SelecionarObjeto** com o argumento do Painel de Navegação definido como **Sim** e use a ação **MinimizarJanela**. O objeto selecionado na ação **SelecionarObjeto** pode ser qualquer objeto no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="da3a6-p103">To hide the Navigation Pane, use the **SelectObject** action with the In Navigation Pane argument set to **Yes** and then use the **MinimizeWindow** action. The object you select in the **SelectObject** action can be any object in the database.</span></span>

  - <span data-ttu-id="da3a6-p104">Você pode ocultar a janela ativa clicando em **Gerenciar Esta Janela** no menu **Exibir** e clicando em **Ocultar**. Em vez de ser reduzida a um ícone, a janela ficará invisível. Use o comando **Reexibir** no mesmo menu para que a janela reapareça. É possível usar a ação **ExecutarComandodeMenu** para executar qualquer um desses comandos com uma macro.</span><span class="sxs-lookup"><span data-stu-id="da3a6-p104">You can hide the active window by clicking **Manage This Window** on the **View** menu, and then clicking **Hide**. Instead of being reduced to an icon, the window becomes invisible. Use the **Unhide** command on the same menu to make the window reappear. You can use the **RunMenuCommand** action to carry out either of these commands from a macro.</span></span>

  - <span data-ttu-id="da3a6-123">Você também pode usar a ação **DefinirValor** para definir a propriedade **Visível** de um formulário para ocultar ou mostrar a janela do formulário.</span><span class="sxs-lookup"><span data-stu-id="da3a6-123">You can also use the **SetValue** action to set a form's **Visible** property to hide or show the form's window.</span></span>

<span data-ttu-id="da3a6-124">Para executar a ação **MinimizarJanela** em um módulo do VBA (Visual Basic for Applications), use o método **Minimizar** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="da3a6-124">To run the **MinimizeWindow** action in a Visual Basic for Applications (VBA) module, use the **Minimize** method of the **DoCmd** object.</span></span>

