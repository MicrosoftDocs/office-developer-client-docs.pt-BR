---
title: Programação ADO VBScript
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e94f4d313a9c43d08c9786c6f27fd49624709249
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863063"
---
# <a name="vbscript-ado-programming"></a>Programação ADO VBScript


**Aplica-se a**: Access 2013 | Office 2013 

## <a name="creating-an-ado-project"></a>Criando um projeto ADO

O Microsoft Visual Basic, Scripting Edition, não oferece suporte a bibliotecas de tipos, portanto, você não precisa fazer referência ao ADO em seu projeto. Consequentemente, nenhum recurso associado, como a conclusão da linha de comando, é permitido. Por padrão, as constantes enumeradas do ADO também não são definidas no VBScript.

No entanto, o ADO fornece dois arquivos que contêm as seguintes definições para serem usadas com o VBScript:

  - Para uso de script do lado do servidor adovbs, que é instalado na unidade c:\\Program Files\\arquivos comuns\\sistema\\ado\\ pasta por padrão.

  - Para uso de script do lado do cliente adcvbs, que é instalado na unidade c:\\Program Files\\arquivos comuns\\sistema\\msdac\\ pasta por padrão.

Você pode copiar e colar constantes definições dos seguintes arquivos em páginas ASP ou, se estiver realizando um script do servidor, copie adovbs arquivo para uma pasta no seu site e fazer referência a ele partir de sua página ASP semelhante a esta:

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a>Criando objetos ADO no VBScript

Não é possível usar a instrução **Dim** para atribuir objetos a um tipo específico no VBScript. Além disso, o VBScript não oferece suporte ao uso da sintaxe **New** com a instrução **Dim** no Visual Basic for Applications. Em vez de usar a função **CreateObject**, você deve chamar:

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a>Exemplos do VBScript

O código a seguir é um exemplo genérico da programação no servidor do VBScript em um arquivo ASP (Active Server Page):

```vb 
 
<%  @LANGUAGE="VBSCRIPT" %> 
<%  Option Explicit %> 
<!--#include File="adovbs.inc"--> 
<HTML> 
    <BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
 
    <!-- Your ASP Code goes here --> 
<% 
Dim Source 
Dim Connect 
Dim Rs1 
     
Source = "SELECT * FROM Authors" 
Connect = "Provider=sqloledb;Data Source=srv;" & _ 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
Rs1.Open Source, Connect, adOpenForwardOnly 
Response.Write("Success!") 
%> 
    </BODY> 
</HTML> 
```

Exemplos mais específicos do VBScript encontram-se na documentação do ADO. Para obter mais informações, consulte [os exemplos de código ADO no Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).

## <a name="differences-between-vbscript-and-visual-basic"></a>Diferenças entre VBScript e Visual Basic

Usar o ADO com o VBScript é como usar o ADO com o Visual Basic de várias maneiras, incluindo o modo como a sintaxe é usada. No entanto, existem algumas diferenças significativas:

- O VBScript oferece suporte somente ao tipo de dados Variant, que pode conter diferentes tipos de dados. É possível armazenar os dados de que você precisa em um tipo de dados Variant, e eles funcionarão adequadamente devido ao desempenho do VBScript. Ele reconhece o tipo exigido pelo ADO e converte o valor em Variant de acordo com a necessidade.

- Não é possível usar `on error goto <label>` no VBScript.

- O VBScript oferece suporte a algumas das funções internas do Visual Basic, como **Msgbox**, **Date** e **IsNumeric**. No entanto, como o VBScript é um subconjunto do Visual Basic, nem todas as funções internas são permitidas. Por exemplo, o VBScript não oferece suporte à função **Format** e às funções E/S de arquivo.

