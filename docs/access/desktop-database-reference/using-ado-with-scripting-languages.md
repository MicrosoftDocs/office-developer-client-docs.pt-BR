---
title: Usando o ADO com linguagens de script
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ffab726a38b5cd6890bff694c52156d3f45a40be
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870377"
---
# <a name="using-ado-with-scripting-languages"></a>Uso do ADO com linguagens de script


**Aplica-se a**: Access 2013, o Office 2013

Em um ambiente de script, o ADO permite expor dados através de um script de servidor. Nesse cenário, o ADO, o provedor OLE DB subjacente que o utiliza e qualquer outro componente necessário para a referência a um repositório de dados específico serão instalados em um servidor que esteja executando o Internet Information Services (IIS). Quando você utiliza o Active Server Pages (ASP), o ADO é um componente referenciado em um script que pode gerar HTML, por exemplo. Esse conteúdo HTML pode ser passado via HTTP para um navegador da web de cliente. Com o uso de scripts, a página da Web pode enviar ações de volta para o script do lado do servidor, permitindo que você atualizar, atravessar ou exibir dados específicos.

## <a name="odbc-data-sources"></a>Fontes de dados ODBC

Uma diferença notável entre um código ADO de script e de não-script é a fonte de dados ODBC, se usada. Para aplicativos não-script, você pode criar um DSN de usuário no Administrador de Fonte de Dados ODBC. Para os scripts executados no IIS, crie um DSN de sistema; caso contrário, os scripts não reconhecerão a fonte de dados criada. Isso aplica-se a qualquer aplicativo de script ADO que utiliza o Microsoft OLE DB Provider for ODBC através do Microsoft IIS.

## <a name="referencing-the-ado-library"></a>Referenciando a biblioteca ADO

N/A com linguagens de script.

## <a name="handling-events"></a>Manipulando eventos

N/A com linguagens de script.

Os tópicos a seguir contêm informações mais específicas sobre como usar o ADO com linguagens de script:

- [Programação ADO JScript](jscript-ado-programming.md)

- [Programação ADO VBScript](vbscript-ado-programming.md)