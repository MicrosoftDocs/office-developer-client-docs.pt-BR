---
title: Programação ADO JScript
TOCTitle: JScript ADO programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 114d4d80836632721f52db0c0cb27eca5ece10f6
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943644"
---
# <a name="jscript-ado-programming"></a><span data-ttu-id="9e194-102">Programação ADO JScript</span><span class="sxs-lookup"><span data-stu-id="9e194-102">JScript ADO programming</span></span>


<span data-ttu-id="9e194-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e194-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="creating-an-ado-project"></a><span data-ttu-id="9e194-104">Criando um projeto ADO</span><span class="sxs-lookup"><span data-stu-id="9e194-104">Creating an ADO Project</span></span>

<span data-ttu-id="9e194-p101">O Microsoft JScript não oferece suporte a bibliotecas de tipos, portanto, você não precisa fazer referência ao ADO em seu projeto. Consequentemente, não há suporte para recursos associados, como a conclusão da linha de comando. Por padrão, as constantes enumeradas do ADO também não são definidas no JScript.</span><span class="sxs-lookup"><span data-stu-id="9e194-p101">Microsoft JScript does not support type libraries, so you do not need to reference ADO in your project. Consequently, no associated features such as command line completion are supported. Also, by default, ADO enumerated constants are not defined in JScript.</span></span>

<span data-ttu-id="9e194-108">No entanto, o ADO fornece dois arquivos que contêm as seguintes definições para serem usadas com o JScript:</span><span class="sxs-lookup"><span data-stu-id="9e194-108">However, ADO provides you with two include files containing the following definitions to be used with JScript:</span></span>

- <span data-ttu-id="9e194-109">Para uso de script do lado do servidor adojavas, que é instalado na unidade c:\\Program Files\\arquivos comuns\\sistema\\ado\\ pasta por padrão.</span><span class="sxs-lookup"><span data-stu-id="9e194-109">For server-side scripting use Adojavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

- <span data-ttu-id="9e194-110">Para uso de script do lado do cliente adcjavas, que é instalado na unidade c:\\Program Files\\arquivos comuns\\sistema\\msdac\\ pasta por padrão.</span><span class="sxs-lookup"><span data-stu-id="9e194-110">For client-side scripting use Adcjavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="9e194-111">Você pode copiar e colar constantes definições dos seguintes arquivos em páginas ASP ou, se estiver realizando um script do servidor, copie o arquivo adojavas para uma pasta no seu site e faz referência a ele a partir de sua página ASP semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="9e194-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adojavas.inc file to a folder on your website and references it from your ASP page like this:</span></span>

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a><span data-ttu-id="9e194-112">Criando objetos ADO em JScript</span><span class="sxs-lookup"><span data-stu-id="9e194-112">Creating ADO Objects in JScript</span></span>

<span data-ttu-id="9e194-113">Use a chamada de função **CreateObject**:</span><span class="sxs-lookup"><span data-stu-id="9e194-113">You must instead use the **CreateObject** function call:</span></span>

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a><span data-ttu-id="9e194-114">Exemplo do JScript</span><span class="sxs-lookup"><span data-stu-id="9e194-114">JScript Example</span></span>

<span data-ttu-id="9e194-115">O código a seguir é um exemplo genérico da programação no servidor do JScript em um arquivo ASP (Active Server Page), que abre um objeto **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="9e194-115">The following code is a generic example of JScript server-side programming in an Active Server Page (ASP) file that opens a **Recordset** object:</span></span>

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

