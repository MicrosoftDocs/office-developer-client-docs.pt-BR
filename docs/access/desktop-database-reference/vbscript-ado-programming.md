---
title: Programação ADO VBScript
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4aff2c8b3394321367851ad82e4e7efe98badff8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306024"
---
# <a name="vbscript-ado-programming"></a><span data-ttu-id="8963d-102">Programação ADO VBScript</span><span class="sxs-lookup"><span data-stu-id="8963d-102">VBScript ADO programming</span></span>


<span data-ttu-id="8963d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8963d-103">**Applies to**: Access 2013, Office 2013</span></span> 

## <a name="creating-an-ado-project"></a><span data-ttu-id="8963d-104">Criando um projeto ADO</span><span class="sxs-lookup"><span data-stu-id="8963d-104">Creating an ADO Project</span></span>

<span data-ttu-id="8963d-p101">O Microsoft Visual Basic, Scripting Edition, não oferece suporte a bibliotecas de tipos, portanto, você não precisa fazer referência ao ADO em seu projeto. Consequentemente, nenhum recurso associado, como a conclusão da linha de comando, é permitido. Por padrão, as constantes enumeradas do ADO também não são definidas no VBScript.</span><span class="sxs-lookup"><span data-stu-id="8963d-p101">Microsoft Visual Basic, Scripting Edition does not support type libraries, so you do not need to reference ADO in your project. Consequently, no associated features such as command line completion are supported. Also, by default, ADO enumerated constants are not defined in VBScript.</span></span>

<span data-ttu-id="8963d-108">No entanto, o ADO fornece dois arquivos que contêm as seguintes definições para serem usadas com o VBScript:</span><span class="sxs-lookup"><span data-stu-id="8963d-108">However, ADO provides you with two include files containing the following definitions to be used with VBScript:</span></span>

  - <span data-ttu-id="8963d-109">Para script no servidor, use o Adovbs. Inc, que é instalado na pasta c:\\arquivos\\de programas comuns\\do\\sistema\\ de arquivos comuns do sistema ADO por padrão.</span><span class="sxs-lookup"><span data-stu-id="8963d-109">For server-side scripting use Adovbs.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

  - <span data-ttu-id="8963d-110">Para scripts do lado do cliente, use o Adcvbs. Inc, que é instalado na pasta\\c:\\arquivos de\\programas\\comuns\\ do sistema de arquivos comuns msdac por padrão.</span><span class="sxs-lookup"><span data-stu-id="8963d-110">For client-side scripting use Adcvbs.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="8963d-111">Você pode copiar e colar definições de constantes desses arquivos nas suas páginas ASP ou, se estiver executando o script no servidor, copiar o arquivo Adovbs. Inc para uma pasta no seu site e fazer referência a ele a partir da página ASP, da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="8963d-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adovbs.inc file to a folder on your website and referencing it from your ASP page like this:</span></span>

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a><span data-ttu-id="8963d-112">Criando objetos ADO no VBScript</span><span class="sxs-lookup"><span data-stu-id="8963d-112">Creating ADO Objects in VBScript</span></span>

<span data-ttu-id="8963d-p102">Não é possível usar a instrução **Dim** para atribuir objetos a um tipo específico no VBScript. Além disso, o VBScript não oferece suporte ao uso da sintaxe **New** com a instrução **Dim** no Visual Basic for Applications. Em vez de usar a função **CreateObject**, você deve chamar:</span><span class="sxs-lookup"><span data-stu-id="8963d-p102">You cannot use the **Dim** statement to assign objects to a specific type in VBScript. Also, VBScript does not support the **New** syntax used with the **Dim** statement in Visual Basic for Applications. You must instead use the **CreateObject** function call:</span></span>

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a><span data-ttu-id="8963d-116">Exemplos do VBScript</span><span class="sxs-lookup"><span data-stu-id="8963d-116">VBScript Examples</span></span>

<span data-ttu-id="8963d-117">O código a seguir é um exemplo genérico da programação no servidor do VBScript em um arquivo ASP (Active Server Page):</span><span class="sxs-lookup"><span data-stu-id="8963d-117">The following code is a generic example of VBScript server-side programming in an Active Server Page (ASP) file:</span></span>

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

<span data-ttu-id="8963d-118">Exemplos mais específicos do VBScript encontram-se na documentação do ADO.</span><span class="sxs-lookup"><span data-stu-id="8963d-118">More specific VBScript examples are included with the ADO documentation.</span></span> <span data-ttu-id="8963d-119">Para obter mais informações, consulte [exemplos de código do ADO no Microsoft Visual Basic scriptIng Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).</span><span class="sxs-lookup"><span data-stu-id="8963d-119">For more information, see [ADO code examples in Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).</span></span>

## <a name="differences-between-vbscript-and-visual-basic"></a><span data-ttu-id="8963d-120">Diferenças entre VBScript e Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8963d-120">Differences Between VBScript and Visual Basic</span></span>

<span data-ttu-id="8963d-p104">Usar o ADO com o VBScript é como usar o ADO com o Visual Basic de várias maneiras, incluindo o modo como a sintaxe é usada. No entanto, existem algumas diferenças significativas:</span><span class="sxs-lookup"><span data-stu-id="8963d-p104">Using ADO with VBScript is similar to using ADO with Visual Basic in many ways, including how syntax is used. However, some significant differences exist:</span></span>

- <span data-ttu-id="8963d-p105">O VBScript oferece suporte somente ao tipo de dados Variant, que pode conter diferentes tipos de dados. É possível armazenar os dados de que você precisa em um tipo de dados Variant, e eles funcionarão adequadamente devido ao desempenho do VBScript. Ele reconhece o tipo exigido pelo ADO e converte o valor em Variant de acordo com a necessidade.</span><span class="sxs-lookup"><span data-stu-id="8963d-p105">VBScript supports only the Variant data type, which can hold different types of data. You can store the data you need in a Variant data type, and the data will function appropriately due to casting performed by VBScript. It recognizes the type required by ADO, and converts the value in the Variant accordingly.</span></span>

- <span data-ttu-id="8963d-126">Não é possível `on error goto <label>` usar no VBScript.</span><span class="sxs-lookup"><span data-stu-id="8963d-126">You cannot use `on error goto <label>` within VBScript.</span></span>

- <span data-ttu-id="8963d-p106">O VBScript oferece suporte a algumas das funções internas do Visual Basic, como **Msgbox**, **Date** e **IsNumeric**. No entanto, como o VBScript é um subconjunto do Visual Basic, nem todas as funções internas são permitidas. Por exemplo, o VBScript não oferece suporte à função **Format** e às funções E/S de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8963d-p106">VBScript supports some of the built-in Visual Basic functions such as **Msgbox**, **Date**, and **IsNumeric**. However, because VBScript is a subset of Visual Basic, not all built-in functions are supported. For example, VBScript does not support the **Format** function and the file I/O functions.</span></span>

