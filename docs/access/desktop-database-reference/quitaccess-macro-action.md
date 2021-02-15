---
title: Ação da macro SairdoAccess
TOCTitle: QuitAccess macro action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 424b2b2cab9bc4272052a201350a0cc2ab297b8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302811"
---
# <a name="quitaccess-macro-action"></a><span data-ttu-id="aaa3a-102">Ação da macro SairdoAccess</span><span class="sxs-lookup"><span data-stu-id="aaa3a-102">QuitAccess macro action</span></span>

<span data-ttu-id="aaa3a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aaa3a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aaa3a-p101">Você pode usar a ação **SairdoAccess** para sair do Microsoft Access. A ação **SairdoAccess** também pode especificar uma das várias opções para salvar objetos de banco de dados antes de sair do Access.</span><span class="sxs-lookup"><span data-stu-id="aaa3a-p101">You can use the **QuitAccess** action to exit Microsoft Access. The **QuitAccess** action can also specify one of several options for saving database objects prior to exiting Access.</span></span>

> [!NOTE]
> <span data-ttu-id="aaa3a-106">Essa ação não será permitida se o banco de dados não for confiável.</span><span class="sxs-lookup"><span data-stu-id="aaa3a-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="aaa3a-107">Setting</span><span class="sxs-lookup"><span data-stu-id="aaa3a-107">Setting</span></span>

<span data-ttu-id="aaa3a-108">A ação **SairdoAccess** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="aaa3a-108">The **QuitAccess** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aaa3a-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="aaa3a-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="aaa3a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="aaa3a-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aaa3a-111"><strong>Opções</strong></span><span class="sxs-lookup"><span data-stu-id="aaa3a-111"><strong>Options</strong></span></span></p></td>
<td><p><span data-ttu-id="aaa3a-p102">Especifica o que acontece com objetos não salvos ao encerrar o Access. Clique em <strong>Aviso</strong> (para exibir caixas de diálogo que perguntam se cada objeto será salvo), <strong>Salvar Tudo</strong> (para salvar todos os objetos sem avisar por caixas de diálogo) ou <strong>Sair</strong> (para encerrar sem salvar nenhum objeto) na caixa <strong>Opções</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. O padrão é <strong>Salvar Tudo</strong>.</span><span class="sxs-lookup"><span data-stu-id="aaa3a-p102">Specifies what happens to unsaved objects when you quit Access. Click <strong>Prompt</strong> (to display dialog boxes that ask whether to save each object), <strong>Save All</strong> (to save all objects without prompting by dialog boxes), or <strong>Exit</strong> (to quit without saving any objects) in the <strong>Options</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Save All</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="aaa3a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="aaa3a-115">Remarks</span></span>

<span data-ttu-id="aaa3a-116">O Access não executa nenhuma ação que siga a ação **SairdoAccess** em uma macro.</span><span class="sxs-lookup"><span data-stu-id="aaa3a-116">Access doesn't run any actions that follow the **QuitAccess** action in a macro.</span></span>

<span data-ttu-id="aaa3a-p103">Você pode usar esta ação para encerrar o Access sem avisos de caixas de diálogo **Salvar** usando um comando de menu personalizado ou um botão de um formulário. Por exemplo, talvez você tenha um formulário mestre usado para exibir os objetos em seu espaço de trabalho personalizado. Esse formulário pode ter um botão **Encerrar** que executa uma macro que contém a ação **SairdoAccess** com o argumento **Opções** definido como **Salvar Tudo**.</span><span class="sxs-lookup"><span data-stu-id="aaa3a-p103">You can use this action to quit Access without prompts from **Save** dialog boxes by using a custom menu command or a button on a form. For example, you might have a master form that you use to display the objects in your custom workspace. This form could have a **Quit** button that runs a macro containing the **QuitAccess** action with the **Options** argument set to **Save All**.</span></span>

<span data-ttu-id="aaa3a-p104">Esta ação equivale a clicar na guia **Arquivo** e clicar em **Sair**. Se você tiver objetos não salvos ao clicar nesse comando, as caixas de diálogo que aparecerem serão as mesmas daquelas exibidas ao usar **Aviso** para o argumento **Opções** da ação **SairdoAccess**.</span><span class="sxs-lookup"><span data-stu-id="aaa3a-p104">This action has the same effect as clicking the **File** tab and then clicking **Exit**. If you have any unsaved objects when you click this command, the dialog boxes that appear are the same as those displayed when you use **Prompt** for the **Options** argument of the **QuitAccess** action.</span></span>

<span data-ttu-id="aaa3a-122">Você pode usar a ação **SalvarObjeto** de uma macro para salvar um objeto especificado sem precisar encerrar o Access ou fechar o objeto.</span><span class="sxs-lookup"><span data-stu-id="aaa3a-122">You can use the **SaveObject** action in a macro to save a specified object without having to quit Access or close the object.</span></span>

<span data-ttu-id="aaa3a-123">Para executar a ação **SairdoAccess** em um módulo do VBA (Visual Basic for Applications), use o método **Sair** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="aaa3a-123">To run the **QuitAccess** action in a Visual Basic for Applications (VBA) module, use the **Quit** method of the **DoCmd** object.</span></span>

