---
title: Ação da macro AbrirProcedimentoArmazenado
TOCTitle: OpenStoredProcedure macro action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b972174e4fe7f3c0384b7483e17eb5ceb9e8bc15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288305"
---
# <a name="openstoredprocedure-macro-action"></a>Ação da macro AbrirProcedimentoArmazenado

**Aplica-se ao:** Access 2013, Office 2013

Em um projeto do Access, você pode usar a ação **AbrirProcedimentoArmazenado** para abrir um procedimento armazenado em modo Folha de Dados, em modo Design de procedimento armazenado ou Visualizar Impressão. Esta ação executa o procedimento armazenado nomeado quando aberta em modo Folha de Dados. Você pode selecionar o modo de entrada de dados do procedimento armazenado e restringir os registros exibidos pelo procedimento armazenado.

> [!NOTE]
> Essa ação não será permitida se o banco de dados não for confiável. 

## <a name="setting"></a>Configuração

A ação **AbrirProcedimentoArmazenado** tem os seguintes argumentos.

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
<td><p><strong>Nome do Procedimento</strong></p></td>
<td><p>O nome do procedimento armazenado que será aberto. A caixa <strong>nome do procedimento</strong> na seção <strong>argumentos da ação</strong> do painel Construtor de macros mostra todos os procedimentos armazenados no banco de dados atual. Esse é um argumento obrigatório. Se você executar uma macro que contém a ação <strong>AbrirProcedimentoArmazenado</strong> em um banco de dados biblioteca, o Microsoft Access procurará o procedimento armazenado com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>O modo de exibição no qual o procedimento armazenado será aberto. Clique em <strong>Folha de Dados</strong>, <strong>Design</strong>, <strong>Visualizar Impressão</strong>, <strong>Tabela Dinâmica</strong> ou <strong>Gráfico Dinâmico</strong> na caixa <strong>Modo de Exibição</strong>. O padrão é <strong>Folha de Dados</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de Dados</strong></p></td>
<td><p>O modo de entrada de dados do procedimento armazenado. Isso se aplica somente a procedimentos armazenados abertos no modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode exibir ou editar os existentes), <strong>Editar</strong> (o usuário pode exibir ou editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentários

Esta ação é semelhante a clicar duas vezes no procedimento armazenado do Painel de Navegação ou a clicar com o botão direito do mouse no procedimento armazenado do Painel de Navegação e selecionar o comando desejado.

Alternar para o modo Design enquanto o procedimento armazenado é aberto remove a configuração do argumento **Modo de Dados** do procedimento armazenado. Essa configuração não entra em vigor, mesmo se o usuário retorna para o modo Folha de Dados.

> [!TIP]
> - Você pode arrastar um procedimento armazenado do painel de navegação para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirProcedimentoArmazenado** que abre o procedimento armazenado em modo Folha de Dados.
> - Se você não deseja exibir as mensagens do sistema que normalmente aparecem quando um procedimento armazenado é executado (indicando que ele é um procedimento armazenado e mostrando quantos registros serão afetados), use a ação **DefinirAviso** para suprimir a exibição dessas mensagens.

Para executar a ação **AbrirProcedimentoArmazenado** em um módulo do VBA (Visual Basic for Applications), use o método **OpenStoredProcedure** do objeto **DoCmd**.

