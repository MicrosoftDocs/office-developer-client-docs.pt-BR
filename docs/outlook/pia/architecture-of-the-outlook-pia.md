---
title: Arquitetura do Outlook PIA
TOCTitle: Architecture of the Outlook PIA
ms:assetid: 89577d14-e6e2-4270-8e72-b0adba378667
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646255(v=office.15)
ms:contentKeyID: 55119777
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 37ecad42b08b96d79d96d62f98e27913a0309971
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336523"
---
# <a name="architecture-of-the-outlook-pia"></a>Arquitetura do Outlook PIA

O Outlook Primary Interop Assembly (PIA) oferece suporte total ao desenvolvimento em relação ao modelo de objeto do Outlook no código gerenciado. No entanto, quando você observa o PIA em um navegador de objetos pela primeira vez, pode se surpreender com as muitas interfaces extras que o PIA contém e com o fato de que nem todos os membros de método, propriedade e evento de um objeto são expostos pela mesma interface de objeto. Os tópicos nesta seção descrevem as diretrizes de como acessar os membros do objeto no código e onde procurar ajuda para objetos, métodos, propriedades e eventos.

## <a name="in-this-section"></a>Nesta seção

|Tópico|Descrição|
|:----|:----------|
|[Associar o Outlook PIA ao modelo de objeto](relating-the-outlook-pia-with-the-object-model.md) |Fornece uma visão geral de como os objetos e membros no modelo de objeto do Outlook baseado em COM são mapeados para as interfaces e classes gerenciadas correspondentes na PIA.|
|[Objetos no Outlook PIA](objects-in-the-outlook-pia.md) |Lista as interfaces, classes e delegados .NET que são mapeados para um objeto COM e descreve como acessar um objeto no PIA.|
|[Métodos e propriedade no Outlook PIA](methods-and-properties-in-the-outlook-pia.md) |Descreve como acessar métodos e propriedades de um objeto em código gerenciado usando o PIA.|
|[Eventos no Outlook PIA](events-in-the-outlook-pia.md) |Descreve interfaces relacionadas a eventos, delegados e classes auxiliares de coletor no PIA.|

## <a name="see-also"></a>Confira também

- [Como realizar a configuração para usar o Outlook PIA](setting-up-to-use-the-outlook-pia.md)
- [Desenvolvimento de suplementos gerenciados do Outlook usando o Outlook PIA](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [Como faço para... (Referência do PIA do Outlook 2013)](how-do-i-outlook-2013-pia-reference.md)

