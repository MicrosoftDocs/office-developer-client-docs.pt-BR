---
title: Usando o ADO com linguagens de script
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 196366987e89f52a3c498a769fa501a3faca9dae
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604432"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="ab362-102">Usando o ADO com linguagens de script</span><span class="sxs-lookup"><span data-stu-id="ab362-102">Using ADO with Scripting Languages</span></span>


<span data-ttu-id="ab362-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab362-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ab362-104"><<<<<<< Cabeça dentro de um ambiente de script, o ADO permite expor os dados por meio de script do servidor.</span><span class="sxs-lookup"><span data-stu-id="ab362-104"><<<<<<< HEAD Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="ab362-105">Nesse cenário, o ADO, o provedor OLE DB subjacente que o utiliza e qualquer outro componente necessário para a referência a um repositório de dados específico serão instalados em um servidor que esteja executando o Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="ab362-105">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="ab362-106">Quando você utiliza o Active Server Pages (ASP), o ADO é um componente referenciado em um script que pode gerar HTML, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="ab362-106">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="ab362-107">Esse conteúdo HTML pode ser passado por HTTP para um navegador cliente.</span><span class="sxs-lookup"><span data-stu-id="ab362-107">This HTML content can be passed via HTTP to a client Web browser.</span></span> <span data-ttu-id="ab362-108">O uso de scripts permite que a página da Web envie ações de volta para o script do servidor, para que você atualize, atravesse ou exiba dados específicos.</span><span class="sxs-lookup"><span data-stu-id="ab362-108">Through the use of scripting, the Web page can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>
<span data-ttu-id="ab362-109">=== Dentro de um ambiente de script, o ADO permite que você expor os dados por meio de script do servidor.</span><span class="sxs-lookup"><span data-stu-id="ab362-109">======= Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="ab362-110">Nesse cenário, o ADO, o provedor OLE DB subjacente que o utiliza e qualquer outro componente necessário para a referência a um repositório de dados específico serão instalados em um servidor que esteja executando o Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="ab362-110">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="ab362-111">Quando você utiliza o Active Server Pages (ASP), o ADO é um componente referenciado em um script que pode gerar HTML, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="ab362-111">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="ab362-112">Esse conteúdo HTML pode ser passado via HTTP para um navegador da web de cliente.</span><span class="sxs-lookup"><span data-stu-id="ab362-112">This HTML content can be passed via HTTP to a client web browser.</span></span> <span data-ttu-id="ab362-113">Com o uso de scripts, a página da Web pode enviar ações de volta para o script do lado do servidor, permitindo que você atualizar, atravessar ou exibir dados específicos.</span><span class="sxs-lookup"><span data-stu-id="ab362-113">Through the use of scripting, the webpage can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>
>>>>>>> <span data-ttu-id="ab362-114">mestre</span><span class="sxs-lookup"><span data-stu-id="ab362-114">master</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="ab362-115">Fontes de dados ODBC</span><span class="sxs-lookup"><span data-stu-id="ab362-115">ODBC Data Sources</span></span>

<span data-ttu-id="ab362-p102">Uma diferença notável entre um código ADO de script e de não-script é a fonte de dados ODBC, se usada. Para aplicativos não-script, você pode criar um DSN de usuário no Administrador de Fonte de Dados ODBC. Para os scripts executados no IIS, crie um DSN de sistema; caso contrário, os scripts não reconhecerão a fonte de dados criada. Isso aplica-se a qualquer aplicativo de script ADO que utiliza o Microsoft OLE DB Provider for ODBC através do Microsoft IIS.</span><span class="sxs-lookup"><span data-stu-id="ab362-p102">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used. For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator. For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created. This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="ab362-120">Referenciando a biblioteca ADO</span><span class="sxs-lookup"><span data-stu-id="ab362-120">Referencing the ADO Library</span></span>

<span data-ttu-id="ab362-121">N/A com linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="ab362-121">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="ab362-122">Manipulando eventos</span><span class="sxs-lookup"><span data-stu-id="ab362-122">Handling events</span></span>

<span data-ttu-id="ab362-123">N/A com linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="ab362-123">N/A with scripting languages.</span></span>

<span data-ttu-id="ab362-124">Os tópicos a seguir contêm informações mais específicas sobre como usar o ADO com linguagens de script:</span><span class="sxs-lookup"><span data-stu-id="ab362-124">The following topics contain more specific information about using ADO with scripting languages:</span></span>

  - [<span data-ttu-id="ab362-125">ADO em VBScript</span><span class="sxs-lookup"><span data-stu-id="ab362-125">ADO in VBScript</span></span>](vbscript-ado-programming.md)

  - [<span data-ttu-id="ab362-126">ADO em JScript</span><span class="sxs-lookup"><span data-stu-id="ab362-126">ADO in JScript</span></span>](jscript-ado-programming.md)

