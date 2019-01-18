---
title: Instalar e fazer referência ao Outlook PIA
TOCTitle: Installing and referencing the Outlook PIA
ms:assetid: b1afd047-dcbb-480f-ba74-993d7d7114cb
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646840(v=office.15)
ms:contentKeyID: 55119774
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 45584ae0a7050aa769368db518c9efcd5db9975a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718200"
---
# <a name="installing-and-referencing-the-outlook-pia"></a>Instalar e fazer referência ao Outlook PIA

O Assembly de Interoperabilidade Primário (PIA) do Outlook deve estar instalado no Cache de Assembly Global (GAC) antes de poder incorporar informações do PIA a um suplemento gerenciado do Outlook. Por padrão, o PIA é instalado automaticamente quando você instala o Office no computador de desenvolvimento. No entanto, se você precisar instalar o PIA separadamente, confira [Configurar o computador para desenvolver soluções do Office](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).


> [!NOTE] 
> Você deve ser um administrador no computador de desenvolvimento para instalar os PIAs do Office.

Após a instalação, se você estiver usando o Visual Studio para criar o projeto gerenciado, adicione uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0. Subsequentemente, no navegador de objetos, no namespace **Microsoft.Office.Interop.Outlook**, você pode ver interfaces gerenciadas no PIA com nomes correspondentes a objetos no modelo de objeto do Outlook.

## <a name="see-also"></a>Confira também

- [Instalar assemblies de interoperabilidade primários do Office](https://docs.microsoft.com/visualstudio/vsto/how-to-install-office-primary-interop-assemblies?view=vs-2017)
- [Arquitetura do Outlook PIA](architecture-of-the-outlook-pia.md)

