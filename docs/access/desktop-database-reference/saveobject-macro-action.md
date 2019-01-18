---
title: Ação da macro SalvarObjeto
TOCTitle: SaveObject macro action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf6fe02616134f864a0e07092951ab9cf49aadbc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701869"
---
# <a name="saveobject-macro-action"></a>Ação da macro SalvarObjeto

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **SalvarObjeto** para salvar um objeto do Access especificado ou, se nenhum estiver especificado, o objeto ativo. Em alguns casos, pode também salvar o objeto ativo com um novo nome (tem o mesmo efeito do comando **Salvar como** na **Barra de Ferramentas de Acesso Rápido**).

> [!NOTE]
> [!OBSERVAçãO] This action will not be allowed if the database is not trusted. 

## <a name="setting"></a>Configuração

A ação **SalvarObjeto** tem os seguintes argumentos.

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
<td><p>O tipo de objeto que você deseja salvar. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong>, na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Para selecionar o objeto ativo, deixe este argumento em branco. Se você selecionar um tipo de objeto no argumento, selecione um nome de objeto existente no argumento <strong>Nome do Objeto</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nome do Objeto</strong></p></td>
<td><p>O nome do objeto a ser salvo. A caixa <strong>Nome do Objeto</strong> mostra todos os objetos no banco de dados do tipo selecionado pelo argumento <strong>Object Type</strong>. Se você deixar vazio o argumento de <strong>Tipo de objeto</strong> , você pode deixar este argumento em branco para salvar o objeto ativo ou, em alguns casos, insira um novo nome neste argumento para salvar o objeto ativo com esse nome. Se digitar um novo nome, você deverá cumprir as convenções de nomeação padrão para objetos do Microsoft Access.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

A ação **SalvarObjeto** funciona em todos os objetos de banco de dados que o usuário possa explicitamente abrir e salvar. O objeto especificado deve estar aberto para que a ação **SalvarObjeto** tenha qualquer efeito no objeto. Essa ação é semelhante à ação de selecionar um objeto e salvá-lo clicando em **Salvar** na **Barra de Ferramentas de Acesso Rápido**. 

Deixar em branco o argumento **Tipo de Objeto** e inserir um novo nome no argumento **Nome do Objeto** tem o mesmo efeito de clicar em **Salvar Como** na **Barra de Ferramentas de Acesso Rápido** e digitar um novo nome para o objeto ativo. O uso da ação **SalvarObjeto** permite que você especifique um objeto a ser salvo e execute um comando **Salvar Como** em uma macro.

> [!NOTE]
> [!OBSERVAçãO] A ação **SalvarObjeto** não pode ser utilizada para salvar nenhum dos seguintes itens com um novo nome:
> - Um formulário no modo formulário ou modo de folha de dados
> - Um relatório no modo Visualizar impressão
> - Um módulo
> - Um modo de exibição do servidor no modo de folha de dados ou no modo Visualizar impressão
> - Página no modo de exibição de página de acesso a um dado
> - Uma tabela no modo folha de dados ou no modo Visualizar impressão
> - Uma consulta no modo folha de dados ou visualizar impressão
> - Um procedimento armazenado no modo folha de dados ou no modo Visualizar impressão

A ação **SalvarObjeto**, esteja ela carregada em uma macro em execução no banco de dados atual ou em um banco de dados biblioteca, sempre salva o objeto especificado ou o objeto ativo do banco de dados em que o objeto foi criado.

Se você salvar o objeto com um novo nome, mas o nome for o mesmo de um objeto existente desse tipo, uma caixa de diálogo perguntará se você deseja substituir o objeto existente. Se tiver definido o argumento **Avisos ativos** da ação **DefinirAvisos** como **Não**, a caixa de diálogo não será exibida e o objeto antigo será automaticamente substituído.

Para executar a ação **SalvarObjeto** em um módulo do VBA (Visual Basic for Applications), use o método **Salvar** do objeto **DoCmd**.

