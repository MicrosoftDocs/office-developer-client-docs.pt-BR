---
title: Ação da macro LocalizarPróximoRegistro
TOCTitle: FindNextRecord macro action
ms:assetid: 57fb6457-9098-4e81-c693-78ccd262ce0b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194307(v=office.15)
ms:contentKeyID: 48544985
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89832
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c92a43ce2f4417fde83a544022a90cfca572bf60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292346"
---
# <a name="findnextrecord-macro-action"></a><span data-ttu-id="2be8a-102">Ação da macro LocalizarPróximoRegistro</span><span class="sxs-lookup"><span data-stu-id="2be8a-102">FindNextRecord macro action</span></span>


<span data-ttu-id="2be8a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2be8a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2be8a-p101">Você pode usar a ação **LocalizarPróximoRegistro** para localizar o próximo registro que atende aos critérios especificados pela ação **EncontrarRegistro** anterior ou o valor na caixa de diálogo **Localizar e Substituir** (na guia **Página Inicial**, clique em **Localizar**). Use a ação **LocalizarPróximoRegistro** para pesquisar registros várias vezes. Por exemplo, você pode se mover sucessivamente por todos os registros para buscar um cliente específico.</span><span class="sxs-lookup"><span data-stu-id="2be8a-p101">You can use the **FindNextRecord** action to find the next record that meets the criteria specified by the previous **FindRecord** action or the value in the **Find and Replace** dialog box (on the **Home** tab, click **Find**). You can use the **FindNextRecord** action to search repeatedly for records. For example, you can move successively through all the records for a specific customer.</span></span>

## <a name="setting"></a><span data-ttu-id="2be8a-107">Setting</span><span class="sxs-lookup"><span data-stu-id="2be8a-107">Setting</span></span>

<span data-ttu-id="2be8a-p102">A ação **LocalizarPróximoRegistro** não tem nenhum argumento. A ação **LocalizarPróximoRegistro** localiza o próximo registro que atende aos critérios definidos pela ação **EncontrarRegistro** ou na caixa de diálogo **Localizar e Substituir**. Os argumentos da ação **EncontrarRegistro** são compartilhados com as opções na caixa de diálogo **Localizar e Substituir**.</span><span class="sxs-lookup"><span data-stu-id="2be8a-p102">The **FindNextRecord** action doesn't have any arguments. The **FindNextRecord** action finds the next record that meets the criteria set either by the **FindRecord** action or in the **Find and Replace** dialog box. The arguments for the **FindRecord** action are shared with the options in the **Find and Replace** dialog box.</span></span>

<span data-ttu-id="2be8a-p103">Para definir os critérios de pesquisa, use a ação **EncontrarRegistro**. Normalmente, digita-se uma ação **EncontrarRegistro** em uma macro e usa-se a ação **LocalizarPróximoRegistro** para localizar registros sucessivos que atendem aos mesmos critérios. Para pesquisar registros somente quando um determinado critério é atendido, você pode digitar uma expressão condicional na coluna **Condição** da linha da ação **LocalizarPróximoRegistro**.</span><span class="sxs-lookup"><span data-stu-id="2be8a-p103">To set the search criteria, use the **FindRecord** action. Typically, you enter a **FindRecord** action in a macro and then use the **FindNextRecord** action to find succeeding records that meet the same criteria. To search for records only when a certain condition is met, you can enter a conditional expression in the **Condition** column of the action row for the **FindNextRecord** action.</span></span>

## <a name="remarks"></a><span data-ttu-id="2be8a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2be8a-114">Remarks</span></span>

<span data-ttu-id="2be8a-115">Esta ação equivale a usar o botão **Localizar Próximo** da caixa de diálogo **Localizar e Substituir**.</span><span class="sxs-lookup"><span data-stu-id="2be8a-115">This action has the same effect as using the **Find Next** button in the **Find and Replace** dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="2be8a-p104">[!OBSERVAçãO] Apesar de a ação **EncontrarRegistro** corresponder ao comando **Localizar** da guia **Página Inicial** para tabelas, consultas e formulários, ela não corresponde ao comando **Localizar** no menu **Editar** da janela Código. Você não pode usar a ação **EncontrarRegistro** ou a ação **LocalizarPróximoRegistro** para pesquisar texto em módulos.</span><span class="sxs-lookup"><span data-stu-id="2be8a-p104">Although the **FindRecord** action corresponds to the **Find** command on the **Home** tab for tables, queries, and forms, it doesn't correspond to the **Find** command on the **Edit** menu in the Code window. You can't use the **FindRecord** action or **FindNextRecord** action to search for text in modules.</span></span>

> [!TIP]
> <span data-ttu-id="2be8a-118">[!DICA] Se você definiu o argumento **Somente Campo Atual** da ação **EncontrarRegistro** como **Sim**, talvez precise usar a ação **IrParaControle** para mover o foco para o controle que contém os dados que está pesquisando antes de usar a ação **LocalizarPróximoRegistro**.</span><span class="sxs-lookup"><span data-stu-id="2be8a-118">If you've set the **Only Current Field** argument of the **FindRecord** action to **Yes**, you may need to use the **GoToControl** action to move the focus to the control containing the data you're searching for before you use the **FindNextRecord** action.</span></span>

<span data-ttu-id="2be8a-p105">Se o texto selecionado no momento for o mesmo do texto de pesquisa quando a ação de macro **LocalizarPróximoRegistro** for executada, a pesquisa começará imediatamente após a seleção, no mesmo campo da seleção e no mesmo registro. Caso contrário, começará no início do registro atual. Isso permite localizar várias instâncias dos mesmos critérios de pesquisa que podem aparecer em um único registro.</span><span class="sxs-lookup"><span data-stu-id="2be8a-p105">If the currently selected text is the same as the search text at the time the **FindNextRecord** macro action is carried out, the search begins immediately following the selection, in the same field as the selection, and in the same record. Otherwise, the search begins at the start of the current record. This enables you to find multiple instances of the same search criteria that might appear in a single record.</span></span>

<span data-ttu-id="2be8a-p106">Entretanto, observe que, se você usar um botão de comando para executar uma macro que contém a ação **LocalizarPróximoRegistro**, a primeira instância dos critérios de pesquisa será localizada várias vezes. Esse comportamento ocorre porque clicar no botão de comando remove o foco do campo que contém o valor correspondente. A ação **LocalizarPróximoRegistro** começará a pesquisar partindo do início do registro. Para evitar esse problema, execute a macro usando uma técnica que não altera o foco, como um botão de barra de ferramentas personalizado ou uma combinação de teclas definida em uma macro AutoKeys. Como alternativa, defina o foco na macro para o campo que contém os critérios de pesquisa antes de executar a ação **LocalizarPróximoRegistro**.</span><span class="sxs-lookup"><span data-stu-id="2be8a-p106">However, note that if you use a command button to run a macro containing the **FindNextRecord** action, the first instance of the search criteria will be found repeatedly. This behavior occurs because clicking the command button removes the focus from the field containing the matching value. The **FindNextRecord** action will then begin searching from the start of the record. To avoid this problem, run the macro by using a technique that doesn't change the focus, such as a custom toolbar button or a key combination defined in an AutoKeys macro. Alternatively, set the focus in the macro to the field containing the search criteria before you carry out the **FindNextRecord** action.</span></span>

<span data-ttu-id="2be8a-127">O mesmo comportamento também ocorre se você usa um botão de comando para executar uma macro que contém a ação **EncontrarRegistro** com o argumento **Localizar Primeiro** definido como **Não**.</span><span class="sxs-lookup"><span data-stu-id="2be8a-127">The same behavior also occurs if you use a command button to run a macro containing the **FindRecord** action with the **Find First** argument set to **No**.</span></span>

<span data-ttu-id="2be8a-128">Para executar a ação **LocalizarPróximoRegistro** em um módulo do Visual Basic for Applications, use o método **EncontrarPróximo** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="2be8a-128">To run the **FindNextRecord** action in a Visual Basic for Applications module, use the **FindNext** method of the **DoCmd** object.</span></span>

