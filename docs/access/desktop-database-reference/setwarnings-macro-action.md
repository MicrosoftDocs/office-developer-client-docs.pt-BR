---
title: Ação da macro DefinirAvisos
TOCTitle: SetWarnings Macro Action
ms:assetid: ff95b919-b1ee-c0a0-851d-71894851bb1d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837313(v=office.15)
ms:contentKeyID: 48548965
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165020
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 573f9c2e4a458c6f48c517c59162ba3473aa8d81
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462699"
---
# <a name="setwarnings-macro-action"></a>Ação da macro DefinirAvisos


**Aplica-se a**: Access 2013 | Office 2013

Use a ação **DefinirAvisos** para ativar ou desativar mensagens do sistema.


> [!NOTE]
> <P>[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</P>



## <a name="setting"></a>Configuração

A ação **DefinirAvisos** tem o argumento a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Avisos ativos</strong></p></td>
<td><p>Especifica se as mensagens do sistema são exibidas. Clique em <strong>Sim</strong> (para ativar mensagens do sistema) ou em <strong>Não</strong> (para desativar mensagens do sistema) na caixa <strong>Avisos ativos</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. O padrão é <strong>Não</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar esta ação para impedir que avisos e caixas de mensagem modais parem a macro. Entretanto, as mensagens de erro serão sempre exibidas. Além disso, o Microsoft Access exibirá todas as caixas de diálogo que exigirem outras entradas que não sejam uma simples escolha de botão (como **OK**, **Cancelar**, **Sim** ou **Não**)  por exemplo, qualquer caixa de diálogo que exija a entrada de texto ou a seleção de uma entre várias opções.

A execução desta ação com o argumento **Avisos ativos** definido como **Não** tem o mesmo efeito de pressionar ENTER sempre que um aviso ou caixa de mensagem é exibido. Geralmente, o botão **OK** ou **Sim** é escolhido em resposta ao aviso ou à mensagem.

Quando a macro é concluída, o Access reativa automaticamente a exibição de mensagens do sistema.

Em geral, a ação **Eco** é utilizada, o que oculta os resultados de uma macro até que ela esteja concluída. Você também pode usar a ação **DefinirAvisos** para ocultar avisos e caixas de mensagem.


> [!WARNING]
> <P>[!CUIDADO] Embora a ação <STRONG>DefinirAvisos</STRONG> possa simplificar as interações com as macros, tenha muito cuidado ao desativar mensagens do sistema. Em algumas situações, a interrupção de uma macro poderá ser conveniente se uma mensagem de aviso for exibida. A menos que você confie no resultado de todas as ações de macro, evite o uso desta ação.</P>



Para executar a ação **DefinirAvisos** em um módulo do VBA (Visual Basic for Applications), use o método **SetWarnings** do objeto **DoCmd**.

