---
title: Ação da macro EnviarSequênciaDeCaracteres
TOCTitle: SendKeys macro action
ms:assetid: 3b06fcfc-ea64-c780-b5fc-6fc72853f524
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192656(v=office.15)
ms:contentKeyID: 48544275
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm183441
f1_categories:
- Office.Version=v15
ms.openlocfilehash: aa029e3a81670746cdc467ddf7578c5900b58b29
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929031"
---
# <a name="sendkeys-macro-action"></a>Ação da macro EnviarSequênciaDeCaracteres


**Aplica-se a**: Access 2013, o Office 2013

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Observação sobre segurança" alt="Security note" /><strong>Observação de segurança</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>
      Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.
</td>
</tr>
</tbody>
</table>


Use a ação **EnviarSequênciadeCaracteres** para enviar pressionamentos de teclas para o Microsoft Access ou para um aplicativos ativo baseado no Windows.


> [!NOTE]
> <P>[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</P>



## <a name="setting"></a>Configuração

A ação **EnviarSequênciaDeCaracteres** tem os seguintes argumentos.

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
<td><p><strong>Pressionamentos de teclas</strong></p></td>
<td><p>Os pressionamentos de teclas a serem processados pelo Access ou pelo aplicativo. Insira-os na caixa <strong>Pressionamentos de Teclas</strong> na seção <strong> Argumentos da Ação</strong> do painel Construtor de Macros. Você pode digitar até 255 caracteres. Este é um argumento obrigatório.</p></td>
</tr>
<tr class="even">
<td><p><strong>Wait</strong></p></td>
<td><p>Especifica se a macro deve ser pausada enquanto os pressionamentos de teclas são processados. Clique em <strong>Sim</strong> (para pausar) ou em <strong>Não</strong> (para não pausar). O padrão é <strong>Não</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O Access processa os pressionamentos de teclas recebidos por meio da ação **EnviarSequênciadeCaracteres** exatamente como se você os tivesse digitado diretamente em uma janela do Access.

Para especificar os pressionamentos de teclas, use a mesma sintaxe que usaria para a instrução **EnviarSequênciadeCaracteres**.


> [!NOTE]
> <P>[!OBSERVAçãO] É possível a ocorrência de erro quando o argumento <STRONG>Pressionamentos de teclas</STRONG> contém sintaxe incorreta, erros ortográficos ou outros valores inadequados para a janela da qual os pressionamentos de teclas são enviados.</P>



Você pode usar esta ação para inserir informações em uma caixa de diálogo, principalmente se não quiser interromper a macro para responder manualmente à caixa de diálogo. Algumas ações do Access, como **ArquivoComCópia** e **EncontrarRegistro**, selecionam automaticamente as opções de algumas caixas de diálogo de uso frequente. Use a ação **EnviarSequênciaDeCaracteres** para selecionar opções em caixas de diálogo de uso menos frequente.


> [!NOTE]
> <UL>
> <LI>
> <P>Como a caixa de diálogo suspende a macro, coloque a ação <STRONG>EnviarSequênciaDeCaracteres</STRONG> antes da ação que abre a caixa de diálogo e defina o argumento <STRONG>Aguardar</STRONG> como <STRONG>Não</STRONG>.</P>
> <LI>
> <P>O intervalo dos pressionamentos de teclas para alcançar o Access ou outro aplicativo pode ser complicado. Por isso, se houver outros métodos (como a ação <STRONG>EncontrarRegistro</STRONG> ) que você possa usar para obter a tarefa desejada, é recomendável usá-lo no lugar da ação <STRONG>EnviarSequênciadeCaracteres</STRONG> para preencher as opções de uma caixa de diálogo.</P></LI></UL>



Se quiser enviar mais de 255 caracteres para o Access ou outro aplicativo baseado no Windows, use várias ações **EnviarSequênciaDeCaracteres** em sucessão, em uma macro.

Se usar a **EnviarSequênciadeCaracteres** para enviar pressionamentos de teclas, isso disparará os eventos **ApertarTecla**, **LiberarTecla** e **PressionarTecla**. O envio de pressionamentos de teclas não ANSI (por exemplo, uma tecla de função) não dispara o evento **PressionarTecla**.

Esta ação não está disponível em um módulo do VBA (Visual Basic for Applications). Em vez disso, use a instrução **SendKeys**.

