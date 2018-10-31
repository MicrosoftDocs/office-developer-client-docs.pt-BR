---
title: Ação de macro FecharJanela
TOCTitle: CloseWindow Macro Action
ms:assetid: ba96bc26-7f3f-fd3d-8d3a-e18bfe90cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822510(v=office.15)
ms:contentKeyID: 48547377
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm64319
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d5ddd1a4b99ec301772690b2815d961676c5a058
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861852"
---
# <a name="closewindow-macro-action"></a>Ação de macro FecharJanela


**Aplica-se a**: Access 2013 | Office 2013

Você pode usar a ação **fecharJanela** para fechar uma guia de documento especificada do Access ou a guia do documento ativo se nenhuma estiver especificada.

## <a name="setting"></a>Configuração

A ação **FecharJanela** tem os seguintes argumentos.

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
<td><p>O tipo de objeto cuja guia de documento você deseja fechar. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Para selecionar a guia de documento ativa, deixe este argumento em branco. 

</p>

> [!NOTE]
> Se você estiver fechando um módulo no Editor do Visual Basic, use **Módulo** no argumento **Tipo de Objeto**.


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Nome do Objeto</strong></p></td>
<td><p>O nome do objeto que será fechado. A caixa <strong>Nome do Objeto</strong> mostra todos os objetos no banco de dados do tipo selecionado pelo argumento <strong>Tipo de Objeto</strong>. Clique no objeto que será fechado. Se você deixar o argumento <strong>Tipo de Objeto</strong> em branco, deixe este argumento em branco também.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Save</strong></p></td>
<td><p>Define se serão salvas as alterações no objeto quando ele estiver fechado. Clique em <strong>Sim</strong> (salvar o objeto), <strong>Não</strong> (fechar o objeto sem salvá-lo) ou <strong>Aviso</strong> (perguntar ao usuário se o objeto deverá ser salvo ou não). O padrão é <strong>Aviso</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

A ação **FecharJanela** funciona em todos os objetos de banco de dados que o usuário pode abrir ou fechar explicitamente. Esta ação equivale a selecionar um objeto e fechá-lo clicando com o botão direito do mouse na guia de documento do objeto e clicando em **Fechar** no menu de atalho ou clicando no botão **Fechar** do objeto.

Se o argumento **Salvar** for definido como **Aviso** e o objeto ainda não tiver sido salvo antes de a ação **FecharJanela** ser executada, uma caixa de diálogo solicitará ao usuário que salve o objeto antes de a macro fechá-lo. Se você tiver definido o argumento **Avisos Ativos** da ação **DefinirAvisos** como **Não**, a caixa de diálogo não será exibida e o objeto será salvo automaticamente.

Para executar a ação **FecharJanela** em um módulo do VBA (Visual Basic for Applications), use o método **FecharJanela** do objeto **DoCmd**.

