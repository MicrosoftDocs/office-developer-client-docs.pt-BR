---
title: Usar um objeto de aplicativo confiável fornecido pelas Ferramentas de Desenvolvedor do Office para Visual Studio
TOCTitle: Using a trusted application object provided by Office Developer Tools for Visual Studio
ms:assetid: 3778122f-f60e-48e7-8e72-f3aef168bae2
ms:mtpsurl: https://msdn.microsoft.com/library/Bb622502(v=office.15)
ms:contentKeyID: 55119787
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f86ad294e894b4faea10d033a069638221f1bd78
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703010"
---
# <a name="using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio"></a>Usar um objeto de aplicativo confiável fornecido pelas Ferramentas de Desenvolvedor do Office para Visual Studio

Se você estiver desenvolvendo um suplemento gerenciado usando as Ferramentas de Desenvolvedor do Office para Visual Studio, use sempre o objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) que é fornecido pelo Visual Studio. 

A menos que você pretenda automatizar uma nova instância do Outlook, não use Novo ou uma nova palavra-chave para criar uma nova instância do Outlook, já que esta instância do objeto **Application** objeto não é confiável sob a perspectiva do Outlook Object Model Guard. 

Se o suplemento usa uma instância não confiável do objeto **Application**, dependendo da versão do Outlook que o cliente esteja executando, o suplemento irá invocar por padrão o Outlook Object Model Guard em um número de membros do modelo de objeto. 

Para saber mais sobre o comportamento do Object Model Guard, confira [Alterações de código de segurança no Outlook 2007](https://msdn.microsoft.com/library/bb226709\(v=office.15\)). Observe que, apesar de o artigo "Alterações de código de segurança no Outlook 2007" se referir aos suplementos COM que são confiáveis por padrão, este design se aplica às versões do Outlook desde o Outlook 2007, e a confiabilidade se aplica aos suplementos gerenciados da mesma maneira. Independentemente de o suplemento ser gerenciado ou não, a confiabilidade é baseada na suposição de que o suplemento usa um objeto **Application** confiável.

