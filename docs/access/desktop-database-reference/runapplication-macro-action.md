---
title: Ação da macro ExecutarAplicativo
TOCTitle: RunApplication macro action
ms:assetid: 29967e6e-c441-b115-3ee6-2299b8a3bc25
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192038(v=office.15)
ms:contentKeyID: 48543885
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm93359
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e7bf54934c6be215b2be5f32160d74fc2b4ab346
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306836"
---
# <a name="runapplication-macro-action"></a>Ação da macro ExecutarAplicativo

**Aplica-se ao:** Access 2013, Office 2013

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Observação de segurança" alt="Security note" /><strong>Observação de Segurança</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Use caution when running executable files or code in macros or applications. Executable files or code can be used to carry out actions that might compromise the security of your computer and data.</td>
</tr>
</tbody>
</table>

Você pode usar a ação **ExecutarAplicativo** para executar, no Microsoft Access, um aplicativo baseado no Microsoft Windows ou no MS-DOS, como Microsoft Excel, Microsoft Word ou Microsoft PowerPoint. Por exemplo, é possível colar os dados de uma planilha do Excel no banco de dados do Access.

> [!NOTE]
> Essa ação não será permitida se o banco de dados não for confiável. 

## <a name="setting"></a>Configuração

A ação **ExecutarAplicativo** tem o seguinte argumento.

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
<td><p><strong>Linha de comando</strong></p></td>
<td><p>A linha de comando é usada para iniciar o aplicativo (incluindo o caminho e todos os demais parâmetros necessários, como as opções que permitem executar o aplicativo em um determinado modo). Digite a linha de comando na caixa <strong>Linha de Comando</strong>, na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Este é um argumento obrigatório.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O aplicativo selecionado com essa ação é carregado e executado em primeiro plano. A macro que contém essa ação continuará a ser executada depois de iniciado o aplicativo.

Você pode transferir dados entre o outro aplicativo e o Access usando o recurso DDE (troca dinâmica de dados) do Microsoft Windows ou a área de transferência. A ação **EnviarSequênciadeCaracteres** pode ser utilizada para enviar pressionamentos de teclas ao outro aplicativo (embora o DDE seja um método mais eficiente de transferência de dados). Também é possível compartilhar dados entre vários aplicativos usando a automação.

Os aplicativos baseados no MS-DOS são executados em uma janela do MS-DOS no ambiente Windows.

Nos sistemas operacionais Windows, há muitas maneiras de executar um aplicativo, incluindo a inicialização do programa no Windows Explorer, usando o comando **Executar** no menu **Iniciar** ou clicando duas vezes em um ícone de programa na Área de Trabalho do Windows.

Não é possível executar a ação **ExecutarAplicativo** em módulos do VBA (Visual Basic for Applications). Em vez disso, use a função **Shell** do VBA.

