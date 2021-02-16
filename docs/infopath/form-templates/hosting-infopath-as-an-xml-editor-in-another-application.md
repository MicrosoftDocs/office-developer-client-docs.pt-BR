---
title: Hospedando o InfoPath como um Editor de XML em outro aplicativo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: O ambiente de edição de formulário do Microsoft InfoPath pode ser hospedado em um aplicativo personalizado do Windows, que permite aos desenvolvedores integrar o ambiente de edição de formulário do InfoPath a aplicativos de linha de negócios.
ms.openlocfilehash: b85e47d506b17982bb883c9d56ea13131807d1cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422576"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a>Hospedando o InfoPath como um Editor de XML em outro aplicativo

O ambiente de edição de formulário do Microsoft InfoPath pode ser hospedado em um aplicativo personalizado do Windows. Esse recurso permite que os desenvolvedores integrem o ambiente de edição de formulário do InfoPath em aplicativos de linha de negócios. Os desenvolvedores que escrevem aplicativos baseados em COM tradicionais podem usar o objeto **InfoPathEditorObject** que está disponível referenciando o IPEDITOR.DLL e os desenvolvedores escrevendo microsoft . Aplicativos baseados em NET podem usar o assembly **Microsoft.Office.InfoPath.FormControl,** que fornece tipos gerenciados com base na interface COM. Os assemblys IPEDITOR.DLL e **Microsoft.Office.InfoPath.FormControl** são instalados junto com o InfoPath na pasta C:\Arquivos de Programas\Microsoft Office\Office15 ou C:\Arquivos de Programas (x86)\Microsoft Office\Office15. 
  
O artigo MSDN, hospedando o InfoPath 2007 Form Editing Environment em um aplicativo de formulário personalizado do Windows, concentra-se no objeto **FormControl** e como incorporá-lo ao seu personalizado . Aplicativos baseados em NET. O download associado ao artigo contém um aplicativo personalizado que fornece funções .NET para replicar o ambiente de edição de formulário do InfoPath por meio do uso de **COM IOleCommandTargets**.
  

