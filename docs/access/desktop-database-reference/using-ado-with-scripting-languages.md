---
title: Usando o ADO com linguagens de script
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1ab0615d1c16900e86a844635fad4ac9a90751a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312037"
---
# <a name="using-ado-with-scripting-languages"></a>Uso do ADO com linguagens de script


**Aplica-se ao:** Access 2013, Office 2013

Em um ambiente de script, o ADO permite expor dados através de um script de servidor. Nesse cenário, o ADO, o provedor OLE DB subjacente que o utiliza e qualquer outro componente necessário para a referência a um repositório de dados específico serão instalados em um servidor que esteja executando o Internet Information Services (IIS). Quando você utiliza o Active Server Pages (ASP), o ADO é um componente referenciado em um script que pode gerar HTML, por exemplo. Esse conteúdo HTML pode ser transmitido via HTTP para um navegador da Web do cliente. Por meio do uso de scripts, a página da Web pode enviar ações de volta para o script do lado do servidor, permitindo que você atualize, percorra ou exiba dados específicos.

## <a name="odbc-data-sources"></a>Fontes de dados ODBC

Uma diferença notável entre um código ADO de script e de não-script é a fonte de dados ODBC, se usada. Para aplicativos não-script, você pode criar um DSN de usuário no Administrador de Fonte de Dados ODBC. Para os scripts executados no IIS, crie um DSN de sistema; caso contrário, os scripts não reconhecerão a fonte de dados criada. Isso aplica-se a qualquer aplicativo de script ADO que utiliza o Microsoft OLE DB Provider for ODBC através do Microsoft IIS.

## <a name="referencing-the-ado-library"></a>Referenciando a biblioteca ADO

N/A com linguagens de script.

## <a name="handling-events"></a>Manipulando eventos

N/A com linguagens de script.

Os tópicos a seguir contêm informações mais específicas sobre como usar o ADO com linguagens de script:

- [Programação do ADO no JScript](jscript-ado-programming.md)

- [Programação do ADO no VBScript](vbscript-ado-programming.md)
