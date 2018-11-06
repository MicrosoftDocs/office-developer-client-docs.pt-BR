---
title: Ação da macro RepetirConsulta
TOCTitle: Requery macro action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e59a1f5ce676ceaa1b0b346a38b4487b3233e514
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997375"
---
# <a name="requery-macro-action"></a>Ação da macro RepetirConsulta

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **RepetirConsulta** para atualizar os dados de um controle especificado no objeto ativo, repetindo a consulta da origem do controle. Se nenhum controle estiver especificado, a ação consultará outra vez a origem do próprio objeto. Use essa ação para verificar se o objeto ativo ou um de seus controles exibe a maioria dos dados atuais.

## <a name="setting"></a>Configuração

A ação **RepetirConsulta** tem os argumentos a seguir.

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
<td><p><strong>Nome do Controle</strong></p></td>
<td><p>O nome do controle a ser atualizado. Insira o nome do controle na caixa <strong>Nome do Controle</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Use somente o nome do controle, e não o identificador totalmente qualificado (como <strong>Formulários</strong>!<em>nomeform</em>!<em>nomedocontrole</em>). Deixe esse argumento em branco para repetir a consulta da origem do objeto ativo. Se o objeto ativo for uma folha de dados ou um conjunto de resultados de consulta, deixe esse argumento em branco.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

A ação **RepetirConsulta** executa um destes procedimentos:

- Refaz a consulta na qual o controle ou objeto se baseia.

- Exibe quaisquer registros novos ou alterados e remove quaisquer registros excluídos da tabela na qual o objeto ou o controle se baseia.

> [!NOTE]
> [!OBSERVAçãO] A ação **RepetirConsulta** não afeta a posição do ponteiro de registro.

Os controles baseados em uma consulta ou tabela incluem:

- Caixas de listagem e Caixas de combinação.

- Controles de subformulário.

- Objetos OLE, tais como gráficos.

- Controles contendo funções de agregação de domínios; por exemplo, **DSoma**.

Se o controle especificado não se basear em uma consulta ou tabela, essa ação forçará o recálculo do controle.

Se você deixar em branco o argumento **Nome do Controle**, a ação **RepetirConsulta** terá o mesmo efeito das teclas SHIFT+F9 quando o objeto tiver o foco. Se um controle de subformulário tiver o foco, essa ação repetirá a consulta somente da origem do subformulário (assim como as teclas SHIFT+F9 fazem).

> [!NOTE]
> [!OBSERVAçãO] A ação **RepetirConsulta** refaz a consulta da origem do controle ou do objeto. Por outro lado, a ação **RedesenharObjeto** redesenha os controles do objeto especificado, mas não repete a consulta do banco de dados nem exibe novos registros. A ação **MostrarTodosRegistros** não só repete a consulta do objeto ativo, mas também remove todos os filtros aplicados, o que a ação **RepetirConsulta** não faz.

Se você quiser repetir a consulta de um controle que não esteja no objeto ativo, use o método **Requery** em um módulo do VBA (Visual Basic for Applications), e não a ação **Requery** ou seu respectivo método **Requery** do objeto **DoCmd**. O método **Requery** do VBA é mais rápido do que a ação **Requery** ou o método **DoCmd.Requery**. Além disso, quando você usa a ação **Requery** ou o método **DoCmd.Requery** o Microsoft Access fecha a consulta e a recarrega do banco de dados, mas quando você usa o método **Requery**, o Access reexecuta a consulta, mas sem fechá-la e recarregá-la. Observe que o objeto de dados do ActiveX (ADO) **RepetirConsulta** método funciona da mesma maneira que o método **Requery** do Access.

