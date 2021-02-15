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
# <a name="jscript-ado-programming"></a><span data-ttu-id="8f902-102">Programação ADO JScript</span><span class="sxs-lookup"><span data-stu-id="8f902-102">JScript ADO programming</span></span>


<span data-ttu-id="8f902-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f902-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="creating-an-ado-project"></a><span data-ttu-id="8f902-104">Criando um projeto ADO</span><span class="sxs-lookup"><span data-stu-id="8f902-104">Creating an ADO Project</span></span>

<span data-ttu-id="8f902-p101">O Microsoft JScript não oferece suporte a bibliotecas de tipos, portanto, você não precisa fazer referência ao ADO em seu projeto. Consequentemente, não há suporte para recursos associados, como a conclusão da linha de comando. Por padrão, as constantes enumeradas do ADO também não são definidas no JScript.</span><span class="sxs-lookup"><span data-stu-id="8f902-p101">Microsoft JScript does not support type libraries, so you do not need to reference ADO in your project. Consequently, no associated features such as command line completion are supported. Also, by default, ADO enumerated constants are not defined in JScript.</span></span>

<span data-ttu-id="8f902-108">No entanto, o ADO fornece dois arquivos que contêm as seguintes definições para serem usadas com o JScript:</span><span class="sxs-lookup"><span data-stu-id="8f902-108">However, ADO provides you with two include files containing the following definitions to be used with JScript:</span></span>

- <span data-ttu-id="8f902-109">Para scripts do lado do servidor, use Adojavas.inc, que é instalado na pasta ado c: Program \\ Files Common Files System \\ \\ \\ ado por \\ padrão.</span><span class="sxs-lookup"><span data-stu-id="8f902-109">For server-side scripting use Adojavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

- <span data-ttu-id="8f902-110">Para scripts do lado do cliente, use o Adcjavas.inc, que é instalado na pasta \\ \\ \\ \\ msdac c: Program Files Common Files System por \\ padrão.</span><span class="sxs-lookup"><span data-stu-id="8f902-110">For client-side scripting use Adcjavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="8f902-111">Você pode copiar e colar definições constantes desses arquivos em suas páginas ASP ou, se estiver fazendo scripts no lado do servidor, copiar o arquivo Adojavas.inc para uma pasta em seu site e fazer referência a ele em sua página ASP da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="8f902-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adojavas.inc file to a folder on your website and references it from your ASP page like this:</span></span>

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a><span data-ttu-id="8f902-112">Criando objetos ADO em JScript</span><span class="sxs-lookup"><span data-stu-id="8f902-112">Creating ADO Objects in JScript</span></span>

<span data-ttu-id="8f902-113">Use a chamada de função **CreateObject**:</span><span class="sxs-lookup"><span data-stu-id="8f902-113">You must instead use the **CreateObject** function call:</span></span>

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a><span data-ttu-id="8f902-114">Exemplo do JScript</span><span class="sxs-lookup"><span data-stu-id="8f902-114">JScript Example</span></span>

<span data-ttu-id="8f902-115">O código a seguir é um exemplo genérico da programação no servidor do JScript em um arquivo ASP (Active Server Page), que abre um objeto **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="8f902-115">The following code is a generic example of JScript server-side programming in an Active Server Page (ASP) file that opens a **Recordset** object:</span></span>

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

