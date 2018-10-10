---
title: Ação de macro LocalizarPróximoRegistro
TOCTitle: FindNextRecord Macro Action
ms:assetid: 57fb6457-9098-4e81-c693-78ccd262ce0b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194307(v=office.15)
ms:contentKeyID: 48544985
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89832
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b58478a67468fa7d00c348066459672bc31c52a7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464551"
---
# <a name="findnextrecord-macro-action"></a><span data-ttu-id="e510f-102">Ação de macro LocalizarPróximoRegistro</span><span class="sxs-lookup"><span data-stu-id="e510f-102">FindNextRecord Macro Action</span></span>


<span data-ttu-id="e510f-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e510f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e510f-p101">Você pode usar a ação **LocalizarPróximoRegistro** para localizar o próximo registro que atende aos critérios especificados pela ação **EncontrarRegistro** anterior ou o valor na caixa de diálogo **Localizar e Substituir** (na guia **Página Inicial**, clique em **Localizar**). Use a ação **LocalizarPróximoRegistro** para pesquisar registros várias vezes. Por exemplo, você pode se mover sucessivamente por todos os registros para buscar um cliente específico.</span><span class="sxs-lookup"><span data-stu-id="e510f-p101">You can use the **FindNextRecord** action to find the next record that meets the criteria specified by the previous **FindRecord** action or the value in the **Find and Replace** dialog box (on the **Home** tab, click **Find**). You can use the **FindNextRecord** action to search repeatedly for records. For example, you can move successively through all the records for a specific customer.</span></span>

## <a name="setting"></a><span data-ttu-id="e510f-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="e510f-107">Setting</span></span>

<span data-ttu-id="e510f-p102">A ação **LocalizarPróximoRegistro** não tem nenhum argumento. A ação **LocalizarPróximoRegistro** localiza o próximo registro que atende aos critérios definidos pela ação **EncontrarRegistro** ou na caixa de diálogo **Localizar e Substituir**. Os argumentos da ação **EncontrarRegistro** são compartilhados com as opções na caixa de diálogo **Localizar e Substituir**.</span><span class="sxs-lookup"><span data-stu-id="e510f-p102">The **FindNextRecord** action doesn't have any arguments. The **FindNextRecord** action finds the next record that meets the criteria set either by the **FindRecord** action or in the **Find and Replace** dialog box. The arguments for the **FindRecord** action are shared with the options in the **Find and Replace** dialog box.</span></span>

<span data-ttu-id="e510f-p103">Para definir os critérios de pesquisa, use a ação **EncontrarRegistro**. Normalmente, digita-se uma ação **EncontrarRegistro** em uma macro e usa-se a ação **LocalizarPróximoRegistro** para localizar registros sucessivos que atendem aos mesmos critérios. Para pesquisar registros somente quando um determinado critério é atendido, você pode digitar uma expressão condicional na coluna **Condição** da linha da ação **LocalizarPróximoRegistro**.</span><span class="sxs-lookup"><span data-stu-id="e510f-p103">To set the search criteria, use the **FindRecord** action. Typically, you enter a **FindRecord** action in a macro and then use the **FindNextRecord** action to find succeeding records that meet the same criteria. To search for records only when a certain condition is met, you can enter a conditional expression in the **Condition** column of the action row for the **FindNextRecord** action.</span></span>

## <a name="remarks"></a><span data-ttu-id="e510f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e510f-114">Remarks</span></span>

<span data-ttu-id="e510f-115">Esta ação equivale a usar o botão **Localizar Próximo** da caixa de diálogo **Localizar e Substituir**.</span><span class="sxs-lookup"><span data-stu-id="e510f-115">This action has the same effect as using the **Find Next** button in the **Find and Replace** dialog box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e510f-p104">[!OBSERVAçãO] Apesar de a ação <STRONG>EncontrarRegistro</STRONG> corresponder ao comando <STRONG>Localizar</STRONG> da guia <STRONG>Página Inicial</STRONG> para tabelas, consultas e formulários, ela não corresponde ao comando <STRONG>Localizar</STRONG> no menu <STRONG>Editar</STRONG> da janela Código. Você não pode usar a ação <STRONG>EncontrarRegistro</STRONG> ou a ação <STRONG>LocalizarPróximoRegistro</STRONG> para pesquisar texto em módulos.</span><span class="sxs-lookup"><span data-stu-id="e510f-p104">Although the <STRONG>FindRecord</STRONG> action corresponds to the <STRONG>Find</STRONG> command on the <STRONG>Home</STRONG> tab for tables, queries, and forms, it doesn't correspond to the <STRONG>Find</STRONG> command on the <STRONG>Edit</STRONG> menu in the Code window. You can't use the <STRONG>FindRecord</STRONG> action or <STRONG>FindNextRecord</STRONG> action to search for text in modules.</span></span></P>




> [!TIP]
> <P><span data-ttu-id="e510f-118">[!DICA] Se você definiu o argumento <STRONG>Somente Campo Atual</STRONG> da ação <STRONG>EncontrarRegistro</STRONG> como <STRONG>Sim</STRONG>, talvez precise usar a ação <STRONG>IrParaControle</STRONG> para mover o foco para o controle que contém os dados que está pesquisando antes de usar a ação <STRONG>LocalizarPróximoRegistro</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="e510f-118">If you've set the <STRONG>Only Current Field</STRONG> argument of the <STRONG>FindRecord</STRONG> action to <STRONG>Yes</STRONG>, you may need to use the <STRONG>GoToControl</STRONG> action to move the focus to the control containing the data you're searching for before you use the <STRONG>FindNextRecord</STRONG> action.</span></span></P>



<span data-ttu-id="e510f-p105">Se o texto selecionado no momento for o mesmo do texto de pesquisa quando a ação de macro **LocalizarPróximoRegistro** for executada, a pesquisa começará imediatamente após a seleção, no mesmo campo da seleção e no mesmo registro. Caso contrário, começará no início do registro atual. Isso permite localizar várias instâncias dos mesmos critérios de pesquisa que podem aparecer em um único registro.</span><span class="sxs-lookup"><span data-stu-id="e510f-p105">If the currently selected text is the same as the search text at the time the **FindNextRecord** macro action is carried out, the search begins immediately following the selection, in the same field as the selection, and in the same record. Otherwise, the search begins at the start of the current record. This enables you to find multiple instances of the same search criteria that might appear in a single record.</span></span>

<span data-ttu-id="e510f-p106">Entretanto, observe que, se você usar um botão de comando para executar uma macro que contém a ação **LocalizarPróximoRegistro**, a primeira instância dos critérios de pesquisa será localizada várias vezes. Esse comportamento ocorre porque clicar no botão de comando remove o foco do campo que contém o valor correspondente. A ação **LocalizarPróximoRegistro** começará a pesquisar partindo do início do registro. Para evitar esse problema, execute a macro usando uma técnica que não altera o foco, como um botão de barra de ferramentas personalizado ou uma combinação de teclas definida em uma macro AutoKeys. Como alternativa, defina o foco na macro para o campo que contém os critérios de pesquisa antes de executar a ação **LocalizarPróximoRegistro**.</span><span class="sxs-lookup"><span data-stu-id="e510f-p106">However, note that if you use a command button to run a macro containing the **FindNextRecord** action, the first instance of the search criteria will be found repeatedly. This behavior occurs because clicking the command button removes the focus from the field containing the matching value. The **FindNextRecord** action will then begin searching from the start of the record. To avoid this problem, run the macro by using a technique that doesn't change the focus, such as a custom toolbar button or a key combination defined in an AutoKeys macro. Alternatively, set the focus in the macro to the field containing the search criteria before you carry out the **FindNextRecord** action.</span></span>

<span data-ttu-id="e510f-127">O mesmo comportamento também ocorre se você usa um botão de comando para executar uma macro que contém a ação **EncontrarRegistro** com o argumento **Localizar Primeiro** definido como **Não**.</span><span class="sxs-lookup"><span data-stu-id="e510f-127">The same behavior also occurs if you use a command button to run a macro containing the **FindRecord** action with the **Find First** argument set to **No**.</span></span>

<span data-ttu-id="e510f-128">Para executar a ação **LocalizarPróximoRegistro** em um módulo do Visual Basic for Applications, use o método **EncontrarPróximo** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="e510f-128">To run the **FindNextRecord** action in a Visual Basic for Applications module, use the **FindNext** method of the **DoCmd** object.</span></span>

