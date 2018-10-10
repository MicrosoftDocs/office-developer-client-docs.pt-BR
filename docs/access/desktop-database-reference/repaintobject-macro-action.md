---
title: Ação da macro RedesenharObjeto
TOCTitle: RepaintObject Macro Action
ms:assetid: e8fa7d0b-578c-5071-2bd5-b772b48637a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836055(v=office.15)
ms:contentKeyID: 48548431
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm195788
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4371ce5482b775ad9c022eeda8202c4b2e0f800d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463885"
---
# <a name="repaintobject-macro-action"></a>Ação da macro RedesenharObjeto


**Aplica-se a**: Access 2013 | Office 2013

Você pode usar a ação **RedesenharObjeto** para concluir todas as atualizações de tela pendentes para um objeto de bancos de dados especificado ou para o objeto de banco de dados ativo, caso não haja nenhum especificado. Essas atualizações incluem todos os recálculos pendentes de controles do objeto.

## <a name="setting"></a>Configuração

A ação **RedesenharObjeto** tem os argumentos a seguir.

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
<td><p>O tipo de objeto a ser redesenhado. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong>, na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Deixe esse argumento em branco para selecionar o objeto ativo.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nome do Objeto</strong></p></td>
<td><p>O nome do objeto a ser redesenhado. A caixa <strong>Nome do Objeto</strong> mostra todos os objetos de banco de dados do tipo selecionado pelo argumento <strong>Tipo de Objeto</strong>. Se você deixar o argumento <strong>Tipo de Objeto</strong> em branco, faça o mesmo com este argumento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Para concluir as atualizações de tela pendentes, o Microsoft Access aguarda a finalização de outras tarefas pendentes. Com esta ação, você pode forçar o redesenho imediato dos controles do objeto especificado. Você pode usar a ação:

  - Quando utilizar a ação **DefinirValor** para alterar valores em vários controles. O Access talvez não mostre as alterações de imediato, principalmente se outros controles (por exemplo, controles calculados) dependerem dos valores dos controles alterados.

  - Quando quiser verificar se o formulário em exibição mostra os dados de todos os controles. Por exemplo, controles contendo objetos OLE não exibem os dados imediatamente após a abertura de um formulário.


> [!NOTE]
> <UL>
> <LI>
> <P>Esta ação não ativa a repetição de consulta do banco de dados, portanto, não mostra registros novos e alterados nem remove registros excluídos da tabela ou da consulta subjacente do objeto. Use a ação <STRONG>Repetir Consulta</STRONG> para consultar outra vez a origem do objeto ou de um de seus controles. Use a ação <STRONG>MostrarTodosRegistros</STRONG> para exibir a maioria dos registros recentes e remover todos os filtros aplicados.</P>
> <LI>
> <P>A ação <STRONG>RedesenharObjeto</STRONG> não tem o mesmo efeito de clicar em <STRONG>Atualizar</STRONG> no grupo <STRONG>Registros</STRONG> da guia <STRONG>Página Inicial</STRONG>, que mostra todas as alterações que você ou outros usuários tenham feito nos registros exibidos no momento, em formulários e folhas de dados.</P></LI></UL>



Para executar a ação **RedesenharObjeto** em um módulo do VBA, use o método **RepaintObject** do objeto **DoCmd**.

