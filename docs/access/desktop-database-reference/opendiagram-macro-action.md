---
title: Ação da macro AbrirDiagrama
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4273d6858ad98b723d66ba32fe3b9aa7c902d31
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719621"
---
# <a name="opendiagram-macro-action"></a>Ação da macro AbrirDiagrama

**Aplica-se a**: Access 2013, o Office 2013

Em um projeto do Access, você pode usar a ação **AbrirDiagrama** para abrir um diagrama de banco de dados no modo Design.

> [!NOTE]
> [!OBSERVAçãO] This action will not be allowed if the database is not trusted. 

## <a name="setting"></a>Configuração

A ação **AbrirDiagrama** tem os argumentos a seguir.

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
<td><p><strong>Nome do Diagrama</strong></p></td>
<td><p>O nome do diagrama de banco de dados para abrir. A caixa <strong>Nome do diagrama</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros mostra todos os diagramas de banco de dados no banco de dados atual. Este é um argumento obrigatório. Se você executar uma macro que contém a ação <strong>AbrirDiagrama</strong> em um banco de dados biblioteca, o Microsoft Access procurará o diagrama com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentários

Esta ação é semelhante a clicar duas vezes em um diagrama de banco de dados do Painel de Navegação ou a clicar com o botão direito do mouse no diagrama de banco de dados do Painel de Navegação e clicar em **Modo Design**.

> [!TIP]
> [!DICA] Você pode arrastar um diagrama de banco de dados do Painel de Navegação para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirDiagrama** que abre o diagrama de banco de dados em modo Design.

Para executar a ação **AbrirDiagrama** em um módulo do VBA (Visual Basic for Applications), use o método **OpenDiagram** do objeto **DoCmd**.

