---
title: Programação ADO JScript
TOCTitle: JScript ADO programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 88a84f6fa3604286ca27651cefc999c96ff41d0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290888"
---
# <a name="jscript-ado-programming"></a>Programação ADO JScript


**Aplica-se ao:** Access 2013, Office 2013


## <a name="creating-an-ado-project"></a>Criando um projeto ADO

O Microsoft JScript não oferece suporte a bibliotecas de tipos, portanto, você não precisa fazer referência ao ADO em seu projeto. Consequentemente, não há suporte para recursos associados, como a conclusão da linha de comando. Por padrão, as constantes enumeradas do ADO também não são definidas no JScript.

No entanto, o ADO fornece dois arquivos que contêm as seguintes definições para serem usadas com o JScript:

- Para scripts do lado do servidor, use Adojavas.inc, que é instalado na pasta ado c: Program \\ Files Common Files System \\ \\ \\ ado por \\ padrão.

- Para scripts do lado do cliente, use o Adcjavas.inc, que é instalado na pasta \\ \\ \\ \\ msdac c: Program Files Common Files System por \\ padrão.

Você pode copiar e colar definições constantes desses arquivos em suas páginas ASP ou, se estiver fazendo scripts no lado do servidor, copiar o arquivo Adojavas.inc para uma pasta em seu site e fazer referência a ele em sua página ASP da seguinte forma:

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a>Criando objetos ADO em JScript

Use a chamada de função **CreateObject**:

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a>Exemplo do JScript

O código a seguir é um exemplo genérico da programação no servidor do JScript em um arquivo ASP (Active Server Page), que abre um objeto **Recordset**:

```javascript 
 
<%  @LANGUAGE="JScript" %> 
<!--#include File="adojavas.inc"--> 
<HTML> 
<BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
<% 
var Source = "SELECT * FROM Authors"; 
var Connect =  "Provider=sqloledb;Data Source=srv;" + 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
var Rs1 = Server.CreateObject( "ADODB.Recordset.2.5" ); 
Rs1.Open(Source,Connect,adOpenForwardOnly); 
Response.Write("Success!"); 
%> 
</BODY> 
</HTML> 
```

