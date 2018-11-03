---
title: Usando o ADO com linguagens de script
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 00854a56428a99a4d033f7959690836f88912c77
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944799"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="b1837-102">Usando o ADO com linguagens de script</span><span class="sxs-lookup"><span data-stu-id="b1837-102">Using ADO with scripting languages</span></span>


<span data-ttu-id="b1837-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1837-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1837-104">Em um ambiente de script, o ADO permite expor dados através de um script de servidor.</span><span class="sxs-lookup"><span data-stu-id="b1837-104">Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="b1837-105">Nesse cenário, o ADO, o provedor OLE DB subjacente que o utiliza e qualquer outro componente necessário para a referência a um repositório de dados específico serão instalados em um servidor que esteja executando o Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="b1837-105">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="b1837-106">Quando você utiliza o Active Server Pages (ASP), o ADO é um componente referenciado em um script que pode gerar HTML, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="b1837-106">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="b1837-107">Esse conteúdo HTML pode ser passado via HTTP para um navegador da web de cliente.</span><span class="sxs-lookup"><span data-stu-id="b1837-107">This HTML content can be passed via HTTP to a client web browser.</span></span> <span data-ttu-id="b1837-108">Com o uso de scripts, a página da Web pode enviar ações de volta para o script do lado do servidor, permitindo que você atualizar, atravessar ou exibir dados específicos.</span><span class="sxs-lookup"><span data-stu-id="b1837-108">Through the use of scripting, the webpage can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="b1837-109">Fontes de dados ODBC</span><span class="sxs-lookup"><span data-stu-id="b1837-109">ODBC Data Sources</span></span>

<span data-ttu-id="b1837-p102">Uma diferença notável entre um código ADO de script e de não-script é a fonte de dados ODBC, se usada. Para aplicativos não-script, você pode criar um DSN de usuário no Administrador de Fonte de Dados ODBC. Para os scripts executados no IIS, crie um DSN de sistema; caso contrário, os scripts não reconhecerão a fonte de dados criada. Isso aplica-se a qualquer aplicativo de script ADO que utiliza o Microsoft OLE DB Provider for ODBC através do Microsoft IIS.</span><span class="sxs-lookup"><span data-stu-id="b1837-p102">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used. For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator. For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created. This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="b1837-114">Referenciando a biblioteca ADO</span><span class="sxs-lookup"><span data-stu-id="b1837-114">Referencing the ADO Library</span></span>

<span data-ttu-id="b1837-115">N/A com linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="b1837-115">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="b1837-116">Manipulando eventos</span><span class="sxs-lookup"><span data-stu-id="b1837-116">Handling events</span></span>

<span data-ttu-id="b1837-117">N/A com linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="b1837-117">N/A with scripting languages.</span></span>

<span data-ttu-id="b1837-118">Os tópicos a seguir contêm informações mais específicas sobre como usar o ADO com linguagens de script:</span><span class="sxs-lookup"><span data-stu-id="b1837-118">The following topics contain more specific information about using ADO with scripting languages:</span></span>

- [<span data-ttu-id="b1837-119">Programação ADO JScript</span><span class="sxs-lookup"><span data-stu-id="b1837-119">JScript ADO Programming</span></span>](jscript-ado-programming.md)

- [<span data-ttu-id="b1837-120">Programação ADO VBScript</span><span class="sxs-lookup"><span data-stu-id="b1837-120">VBScript ADO Programming</span></span>](vbscript-ado-programming.md)