---
title: Ação de macro NavegarPara
TOCTitle: NavigateTo Macro Action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6cb9505eaf4a2002b0a4ae73ce4917ac250cda12
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876054"
---
# <a name="navigateto-macro-action"></a>Ação de macro NavegarPara


**Aplica-se a**: Access 2013, o Office 2013

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
<td><p><strong>Category</strong></p></td>
<td><p>Obrigatório. A categoria pela qual você deseja que o Painel de Navegação exiba os objetos. Clique em <strong>Tipo de Objeto</strong>, <strong>Tabelas e Exibições</strong>, <strong>Data de Modificação</strong>, <strong>Data de Criação</strong> ou <strong>Personalizado</strong> na caixa <strong>Categoria</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Group</strong></p></td>
<td><p>Opcional. Os limites de argumento do <strong>grupo</strong> que objetos na categoria aparecem no painel de navegação. Se você deixar vazio o argumento de <strong>grupo</strong> , o painel de navegação exibe todos os objetos de banco de dados, classificados por critérios especificados no argumento <strong>categoria</strong> . Exemplos de argumentos  <strong>Grupo</strong> válidos para os vários argumentos <strong>Categoria</strong> são mostrados na tabela a seguir.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

  - Esta ação é semelhante à seleção de categorias e grupos na barra de título do Painel de Navegação.

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
> <P>[!OBSERVAçãO] Para navegar até o nível superior de uma categoria (por exemplo, <STRONG>Todas as Tabelas</STRONG>, <STRONG>Todos os Objetos do Access</STRONG> ou <STRONG>Todas as Datas</STRONG>), é necessário deixar o argumento Grupo em branco. Por exemplo, quando o argumento <STRONG>Categoria</STRONG> é <STRONG>Tipo de Objeto</STRONG>, a inserção de <STRONG>Todos os Objetos do Access</STRONG> como um argumento <STRONG>Grupo</STRONG> resulta em erro.</P>


