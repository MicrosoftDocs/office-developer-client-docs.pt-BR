---
title: Ação da macro SelecionarObjeto
TOCTitle: SelectObject macro action
ms:assetid: a90539a0-c5a0-e997-9c25-e0972d28f2a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821420(v=office.15)
ms:contentKeyID: 48546914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm41840
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6287bc8a66858d51d65c37477eed7a86cd7839af
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721847"
---
# <a name="selectobject-macro-action"></a>Ação da macro SelecionarObjeto

**Aplica-se a**: Access 2013, o Office 2013

Use a ação **SelecionarObjeto** para selecionar um objeto de banco de dados especificado.

## <a name="setting"></a>Configuração

A ação **SelecionarObjeto** tem os seguintes argumentos.

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
<td><p><strong>Tipo de Objeto</strong></p></td>
<td><p>O tipo de objeto de banco de dados a ser selecionado. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong>, na seção <strong>Argumentos da Ação</strong> do Construtor de Macros. Este é um argumento obrigatório.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nome do Objeto</strong></p></td>
<td><p>O nome do objeto a ser selecionado. A caixa <strong>Nome do Objeto</strong> mostra todos os objetos do banco de dados, do tipo selecionado pelo argumento <strong>Tipo de objeto</strong>. Este é um argumento obrigatório, a menos que, no Painel de Navegação, você defina o argumento como <strong>Sim</strong>.</p><p><strong>Observação</strong>: os nomes de objeto para objetos de <STRONG>Exibição do servidor</STRONG>, <STRONG>diagrama</STRONG>ou <STRONG>Procedimento armazenado</STRONG> não são exibidos na caixa <STRONG>Nome do objeto</STRONG> de um projeto do Access (. adp).</p></td>
</tr>
<tr class="odd">
<td><p><strong>No Painel de Navegação</strong></p></td>
<td><p>Especifica se o Microsoft Access seleciona o objeto no Painel de Navegação. Clique em <strong>Sim</strong> (para selecionar o objeto nesse painel) ou em <strong>Não</strong> (para não selecionar o objeto no Painel de Navegação). O padrão é <strong>Não</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

A ação **SelecionarObjeto** trabalha com qualquer objeto do Access que possa receber o foco. Essa ação aplica o foco no objeto especificado e, caso o objeto esteja oculto, mostra o objeto. Se o objeto for um formulário, a ação **SelecionarObjeto** definirá a propriedade **Visível** do objeto como **Sim** e retornará o formulário ao modo definido pelas respectivas propriedades do formulário (por exemplo, como um formulário modal ou pop-up).

Se o objeto não for aberto em uma das outras janelas do Access, você poderá selecioná-lo no Painel de Navegação definindo o argumento **No Painel de Navegação** como **Sim**. Se você definir o argumento **No Painel de Navegação** como **Não**, uma mensagem de erro aparecerá quando você tentar selecionar um objeto não aberto.

Geralmente é possível usar essa ação para selecionar um objeto em que você deseja executar ações adicionais. Por exemplo, se tiver configurado o Access para usar janelas sobrepostas, em vez de documentos com guias, você poderá restaurar um objeto que tenha sido minimizado (usando a ação **RestaurarJanela** ) ou maximizar uma janela que contenha um objeto com o qual queira trabalhar (usando a ação **MaximizarJanela** ).

Ao selecionar um formulário, use as ações **IrParaControle**, **IrParaRegistro** e **IrParaPágina** para ir para áreas específicas do formulário. A ação **IrParaRegistro** também funciona em folhas de dados.

Para executar a ação **SelecionarObjeto** em um módulo do VBA (Visual Basic for Applications), use o método **SelectObject** do objeto **DoCmd**.

