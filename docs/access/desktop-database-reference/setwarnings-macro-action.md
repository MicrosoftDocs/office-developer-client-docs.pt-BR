---
title: Ação da macro DefinirAvisos
TOCTitle: SetWarnings macro action
ms:assetid: ff95b919-b1ee-c0a0-851d-71894851bb1d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837313(v=office.15)
ms:contentKeyID: 48548965
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165020
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: acf541bde41c282b752532cb74d5ec4fa4a13ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308656"
---
# <a name="setwarnings-macro-action"></a>Ação da macro DefinirAvisos

**Aplica-se ao:** Access 2013, Office 2013

Use a ação **DefinirAvisos** para ativar ou desativar mensagens do sistema.

> [!NOTE]
> Essa ação não será permitida se o banco de dados não for confiável. 

## <a name="setting"></a>Setting

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
> [!CUIDADO] Embora a ação **DefinirAvisos** possa simplificar as interações com as macros, tenha muito cuidado ao desativar mensagens do sistema. Em algumas situações, a interrupção de uma macro poderá ser conveniente se uma mensagem de aviso for exibida. A menos que você confie no resultado de todas as ações de macro, evite o uso desta ação.

Para executar a ação **DefinirAvisos** em um módulo do VBA (Visual Basic for Applications), use o método **SetWarnings** do objeto **DoCmd**.

