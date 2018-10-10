---
title: Ação de macro RegistrarEvento
TOCTitle: LogEvent Macro Action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f626dd61782baed2e46aa931891a172fc53c1bde
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464046"
---
# <a name="logevent-macro-action"></a>Ação de macro RegistrarEvento


**Aplica-se a**: Access 2013 | Office 2013

A ação **RegistrarEvento** grava informações na tabela de sistema **USysApplicationLog**.


> [!NOTE]
> <P>[!OBSERVAçãO] A ação <STRONG>RegistrarEvento</STRONG> está disponível somente em Macros de Dados.</P>



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

