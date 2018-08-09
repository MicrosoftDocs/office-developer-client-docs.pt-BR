---
title: Hospedar o InfoPath como um Editor de XML em outro aplicativo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: O ambiente de edição de formulários do Microsoft InfoPath podem ser hospedado em um aplicativo personalizado do Windows, que permite aos desenvolvedores integrar o ambiente em aplicativos de linha de negócios de edição de formulários do InfoPath.
ms.openlocfilehash: dd87cba7219b5647bd2b20dd67c6eb0f1811cc59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765595"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a>Hospedar o InfoPath como um Editor de XML em outro aplicativo

O ambiente de edição de formulários do Microsoft InfoPath podem ser hospedado em um aplicativo personalizado do Windows. Esse recurso permite aos desenvolvedores integrar o ambiente em aplicativos de linha de negócios de edição de formulários do InfoPath. Os desenvolvedores que criam aplicativos baseados em COM tradicionais podem usar o objeto de **InfoPathEditorObject** que está disponível pela referência a IPEDITOR. DLL e os desenvolvedores que criam a Microsoft. Aplicativos baseados em NET podem usar o assembly **Microsoft.Office.InfoPath.FormControl** , que fornece tipos gerenciados com base na interface COM. O IPEDITOR. DLL e assembly **Microsoft.Office.InfoPath.FormControl** são instalados, juntamente com o InfoPath no C:\Program Files\Microsoft Office\Office15 ou arquivos C:\Program (x86) \Microsoft Office\Office15 pasta. 
  
O artigo MSDN, hospedando o ambiente de edição de formulário do InfoPath 2007 em um aplicativo de formulário personalizado do Windows, enfoca o objeto **FormControl** e como incorporá-la em seu personalizado. Aplicativos baseados em NET. O download associado ao artigo contém um aplicativo personalizado que fornece funções de .NET para replicar o ambiente devido ao uso COM **IOleCommandTargets**de edição de formulários do InfoPath.
  

