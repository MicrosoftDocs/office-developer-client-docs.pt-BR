---
title: Criar um arquivo de configuração de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 97ecafb2e4159c680fd23607f5ed6f8ea3156de7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425215"
---
# <a name="creating-a-form-configuration-file"></a>Criar um arquivo de configuração de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um arquivo de configuração de formulário fornece informações sobre um formulário tanto para o gerente de formulários como usado como para aplicativos clientes. Um arquivo de configuração de formulário contém uma ampla especificação para um formulário, incluindo as propriedades publicadas pelo formulário para uso por clientes de mensagens, os verbos implementados pelo formulário e as plataformas suportadas pelo formulário.
  
Um arquivo de configuração de formulário é um arquivo com uma extensão. cfg e tem um formato semelhante a um arquivo de inicialização do Windows. É um arquivo de texto sem formatação com várias seções. Cada seção começa com um nome de seção, entre colchetes. Cada seção contém uma ou mais linhas que definem valores e configurações relevantes para essa seção. Os valores têm um dos seguintes tipos:
  
- String
    
- Cadeia de caracteres exibida
    
- Cadeia de caracteres de plataforma
    
- Nome do caminho
    
- Inteiro
    
- GUID
    
Para obter mais informações sobre as seções de um arquivo. cfg, consulte [formato de arquivo dos arquivos de configuração de formulário](file-format-of-form-configuration-files.md).
  
## <a name="see-also"></a>Confira também



[Desenvolver servidores de formulário MAPI](developing-mapi-form-servers.md)

