---
title: Ação da macro RegistrarEvento
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edc2fcaa72f6bfb912708948903aa09b25447580
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998166"
---
# <a name="logevent-macro-action"></a>Ação da macro RegistrarEvento

**Aplica-se a**: Access 2013, o Office 2013

A ação **RegistrarEvento** grava informações na tabela de sistema **USysApplicationLog**.

> [!NOTE]
> [!OBSERVAçãO] A ação **RegistrarEvento** está disponível somente em Macros de Dados.

## <a name="setting"></a>Configuração

A ação **RegistrarEvento** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Obrigatório</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Descrição</strong></p></td>
<td><p>Não</p></td>
<td><p>Uma expressão de cadeia de caracteres que descreve a condição que você deseja registrar. A descrição não deve ultrapassar 255 caracteres.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentários

A ação **RegistrarEvento** que pode ser usada para gravar informações de status na tabela de sistema **USysApplicationLog** sem a necessidade de usar a ação **[GerarErro](raiseerror-macro-action.md)** para exibir um erro. Por exemplo, é possível registrar alterações em um campo específico ou usar os itens gravados em **USysApplicationLog** para auxiliar na depuração da macro.

Quando você usa a ação **RegistrarEvento** para gravar na tabela **USysApplicationLog**, a coluna **Categoria** é automaticamente definida como **Usuário**.

Para ver a tabela **USysApplicationLog**, siga estas etapas:

1.  Clique no menu **Arquivo** e clique em **Opções**.

2.  Na caixa de diálogo **Opções do Access**, clique na guia **Banco de Dados Atual**.

3.  Na seção **Navegação**, clique em **Opções de Navegação**.

4.  Na caixa de diálogo **Opções de Navegação**, clique em **Mostrar Objetos do Sistema** e clique em **OK**.

5.  Clique em **OK** para fechar a caixa de diálogo **Opções do Access**.

