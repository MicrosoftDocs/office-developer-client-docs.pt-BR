---
title: Ação de macro SairdoAccess
TOCTitle: QuitAccess Macro Action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5fa3b7ffc97f69b1ebc85799a8b2a27b6acc1d90
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462141"
---
# <a name="quitaccess-macro-action"></a><span data-ttu-id="2eb82-102">Ação de macro SairdoAccess</span><span class="sxs-lookup"><span data-stu-id="2eb82-102">QuitAccess Macro Action</span></span>


<span data-ttu-id="2eb82-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2eb82-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2eb82-p101">Você pode usar a ação **SairdoAccess** para sair do Microsoft Access. A ação **SairdoAccess** também pode especificar uma das várias opções para salvar objetos de banco de dados antes de sair do Access.</span><span class="sxs-lookup"><span data-stu-id="2eb82-p101">You can use the **QuitAccess** action to exit Microsoft Access. The **QuitAccess** action can also specify one of several options for saving database objects prior to exiting Access.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2eb82-p102">[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span><span class="sxs-lookup"><span data-stu-id="2eb82-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="2eb82-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="2eb82-108">Setting</span></span>

<span data-ttu-id="2eb82-109">A ação **SairdoAccess** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="2eb82-109">The **QuitAccess** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2eb82-110">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="2eb82-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2eb82-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="2eb82-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2eb82-112"><strong>Options</strong></span><span class="sxs-lookup"><span data-stu-id="2eb82-112"><strong>Options</strong></span></span></p></td>
<td><p><span data-ttu-id="2eb82-p103">Especifica o que acontece com objetos não salvos ao encerrar o Access. Clique em <strong>Aviso</strong> (para exibir caixas de diálogo que perguntam se cada objeto será salvo), <strong>Salvar Tudo</strong> (para salvar todos os objetos sem avisar por caixas de diálogo) ou <strong>Sair</strong> (para encerrar sem salvar nenhum objeto) na caixa <strong>Opções</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. O padrão é <strong>Salvar Tudo</strong>.</span><span class="sxs-lookup"><span data-stu-id="2eb82-p103">Specifies what happens to unsaved objects when you quit Access. Click <strong>Prompt</strong> (to display dialog boxes that ask whether to save each object), <strong>Save All</strong> (to save all objects without prompting by dialog boxes), or <strong>Exit</strong> (to quit without saving any objects) in the <strong>Options</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Save All</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2eb82-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2eb82-116">Remarks</span></span>

<span data-ttu-id="2eb82-117">O Access não executa nenhuma ação que siga a ação **SairdoAccess** em uma macro.</span><span class="sxs-lookup"><span data-stu-id="2eb82-117">Access doesn't run any actions that follow the **QuitAccess** action in a macro.</span></span>

<span data-ttu-id="2eb82-p104">Você pode usar esta ação para encerrar o Access sem avisos de caixas de diálogo **Salvar** usando um comando de menu personalizado ou um botão de um formulário. Por exemplo, talvez você tenha um formulário mestre usado para exibir os objetos em seu espaço de trabalho personalizado. Esse formulário pode ter um botão **Encerrar** que executa uma macro que contém a ação **SairdoAccess** com o argumento **Opções** definido como **Salvar Tudo**.</span><span class="sxs-lookup"><span data-stu-id="2eb82-p104">You can use this action to quit Access without prompts from **Save** dialog boxes by using a custom menu command or a button on a form. For example, you might have a master form that you use to display the objects in your custom workspace. This form could have a **Quit** button that runs a macro containing the **QuitAccess** action with the **Options** argument set to **Save All**.</span></span>

<span data-ttu-id="2eb82-p105">Esta ação equivale a clicar na guia **Arquivo** e clicar em **Sair**. Se você tiver objetos não salvos ao clicar nesse comando, as caixas de diálogo que aparecerem serão as mesmas daquelas exibidas ao usar **Aviso** para o argumento **Opções** da ação **SairdoAccess**.</span><span class="sxs-lookup"><span data-stu-id="2eb82-p105">This action has the same effect as clicking the **File** tab and then clicking **Exit**. If you have any unsaved objects when you click this command, the dialog boxes that appear are the same as those displayed when you use **Prompt** for the **Options** argument of the **QuitAccess** action.</span></span>

<span data-ttu-id="2eb82-123">Você pode usar a ação **SalvarObjeto** de uma macro para salvar um objeto especificado sem precisar encerrar o Access ou fechar o objeto.</span><span class="sxs-lookup"><span data-stu-id="2eb82-123">You can use the **SaveObject** action in a macro to save a specified object without having to quit Access or close the object.</span></span>

<span data-ttu-id="2eb82-124">Para executar a ação **SairdoAccess** em um módulo do VBA (Visual Basic for Applications), use o método **Sair** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="2eb82-124">To run the **QuitAccess** action in a Visual Basic for Applications (VBA) module, use the **Quit** method of the **DoCmd** object.</span></span>

