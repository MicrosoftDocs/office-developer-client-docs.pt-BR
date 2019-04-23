---
title: Ação da macro NavegarPara
TOCTitle: NavigateTo macro action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1c37e798e0624a5655b63a76332073e5b57c0823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288599"
---
# <a name="navigateto-macro-action"></a>Ação da macro NavegarPara

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **NavegarPara** para controlar a exibição de objetos de banco de dados no Painel de Navegação. Por exemplo, é possível alterar a maneira como os objetos de banco de dados são categorizados, além de filtrá-los para que somente alguns sejam exibidos.

## <a name="setting"></a>Configuração

A ação **NavegarPara** tem os seguintes argumentos.

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
<td><p><strong>Categoria</strong></p></td>
<td><p>Obrigatório. A categoria pela qual você deseja que o Painel de Navegação exiba os objetos. Clique em <strong>Tipo de Objeto</strong>, <strong>Tabelas e Exibições</strong>, <strong>Data de Modificação</strong>, <strong>Data de Criação</strong> ou <strong>Personalizado</strong> na caixa <strong>Categoria</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Group</strong></p></td>
<td><p>Opcional. O argumento <strong>Grupo</strong> limita quais objetos na categoria aparecem no Painel de Navegação. Se você deixar o argumento <strong>grupo</strong> em branco, o painel de navegação exibirá todos os objetos de banco de dados, categorizados pelos critérios especificados no argumento <strong>Category</strong> . Exemplos de argumentos <strong>Grupo</strong> válidos para os vários argumentos <strong>Categoria</strong> são mostrados na tabela a seguir.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

- Esta ação é semelhante à seleção de categorias e grupos na barra de título do painel de navegação.

- Os argumentos **Grupo** válidos dependem do argumento **Categoria** usado. Se você digitar um argumento **Grupo** inválido, será exibida uma mensagem de erro.A tabela a seguir contém exemplos de argumentos **Grupo** válidos para cada argumento **Categoria**.
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p>Argumento Categoria</p></th>
  <th><p>Argumentos Grupo de exemplo</p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p>Tipo de Objeto</p></td>
  <td><p>Tabelas; Formulários; Consultas; Páginas; Macros; Módulos</p></td>
  </tr>
  <tr class="even">
  <td><p>Tabelas e Exibições</p></td>
  <td><p>Nomes de tabelas específicas do banco de dados</p></td>
  </tr>
  <tr class="odd">
  <td><p>Data de Modificação</p></td>
  <td><p>Hoje; Ontem; Mês Passado; Mais Antiga</p></td>
  </tr>
  <tr class="even">
  <td><p>Data de Criação</p></td>
  <td><p>Hoje; Ontem; Mês Passado; Mais Antiga</p></td>
  </tr>
  <tr class="odd">
  <td><p>Categoria Personalizado</p></td>
  <td><p>Nomes de grupos que você criou para a categoria personalizada especificada</p></td>
  </tr>
  </tbody>
  </table>

- Para executar a ação **NavegarPara** em um módulo do VBA, use o método **NavigateTo** do objeto **DoCmd**.

> [!NOTE]
> [!OBSERVAçãO] Para navegar até o nível superior de uma categoria (por exemplo, **Todas as Tabelas**, **Todos os Objetos do Access** ou **Todas as Datas**), é necessário deixar o argumento Grupo em branco. Por exemplo, quando o argumento **Categoria** é **Tipo de Objeto**, a inserção de **Todos os Objetos do Access** como um argumento **Grupo** resulta em erro.


