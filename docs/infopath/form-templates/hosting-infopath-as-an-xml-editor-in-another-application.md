---
title: Hospedando o InfoPath como um editor de XML em outro aplicativo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: O ambiente de edição de formulário do Microsoft InfoPath pode ser hospedado em um aplicativo do Windows personalizado, que permite que os desenvolvedores integrem o ambiente de edição de formulários do InfoPath em aplicativos de linha de negócios.
ms.openlocfilehash: b85e47d506b17982bb883c9d56ea13131807d1cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422576"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a>Hospedando o InfoPath como um editor de XML em outro aplicativo

O ambiente de edição de formulário do Microsoft InfoPath pode ser hospedado em um aplicativo do Windows personalizado. Este recurso permite que os desenvolvedores integrem o ambiente de edição de formulários do InfoPath em aplicativos de linha de negócios. Os desenvolvedores que escrevem aplicativos tradicionais baseados em COM podem usar o objeto **InfoPathEditorObject** que está disponível referenciando o IPEDITOR. DLL e desenvolvedores que escrevem o Microsoft. Os aplicativos baseados em rede podem usar o assembly **Microsoft. Office. InfoPath. FormControl** , que fornece tipos gerenciados baseados na interface com. O IPEDITOR. DLL e **Microsoft. Office. InfoPath. FormControl** estão instalados juntamente com o InfoPath na pasta C:\Arquivos de Programas\Microsoft Office\Office15 ou C:\Arquivos de programas (x86) \Microsoft Office\Office15. 
  
O artigo do MSDN, que hospeda o ambiente de edição de formulários do InfoPath 2007 em um aplicativo do Windows Form personalizado, se concentra no objeto **FormControl** e como incorporá-lo ao seu personalizado. Aplicativos baseados em rede. O download associado ao artigo contém um aplicativo personalizado que fornece funções do .NET para a replicação do ambiente de edição de formulários do InfoPath por meio do uso do COM **IOleCommandTargets**.
  

