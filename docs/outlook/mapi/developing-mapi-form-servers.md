---
title: Desenvolver servidores de formulário MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338525"
---
# <a name="developing-mapi-form-servers"></a>Desenvolver servidores de formulário MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Esta seção descreve o processo de criação de arquivos executáveis e de configuração de formulário do servidor de formulários para a criação de formulários MAPI personalizados. Antes de ler esta seção, familiarize-se com as informações em [formulários MAPI](mapi-forms.md).
  
O desenvolvimento de um servidor de formulários inclui as seguintes etapas:
  
1. Decidir quais informações o formulário conterá e escolher um conjunto de propriedades para manter essas informações. Para obter mais informações, consulte [escolhendo o conjunto de propriedades de um formulário](choosing-a-form-s-property-set.md).
    
2. Criar uma interface do usuário com a qual os usuários podem interagir com as propriedades do formulário.
    
3. Escolher uma classe de mensagem e gerar um identificador de classe exclusivo (CLSID). Para obter uma visão geral das classes de mensagens, consulte [MAPI Message classes](mapi-message-classes.md). Para obter mais informações sobre classes e formulários de mensagens, consulte [escolhendo uma classe de mensagem](choosing-a-message-class.md).
    
4. Implementar as interfaces de formulário MAPI necessárias, bem como qualquer interface opcional que seu servidor de formulário específico precise. Para obter mais informações, consulte [Writing Form Server Code](writing-form-server-code.md). 
    
5. Escrever o código de interface do usuário para lidar com a interação do usuário com o objeto Form e as propriedades que o formulário usa.
    
6. Criar um arquivo de configuração de formulário para o formulário. Para obter mais informações, consulte [formato de arquivo dos arquivos de configuração de formulário](file-format-of-form-configuration-files.md).
    
7. Instalar o formulário nos computadores dos usuários. Para obter mais informações, consulte [instalando um formulário em uma biblioteca](installing-a-form-into-a-library.md).
    
Você provavelmente executará as etapas de 1 a 5 simultaneamente, em vez de concluí-las em sequência. O processo de desenvolvimento de um servidor de formulários, como muitos projetos de programação, não é um no qual há uma sequência muito bem definida. Por exemplo, a criação de um arquivo de configuração de formulário é mostrada como a segunda etapa acima, mas você provavelmente criará o arquivo de configuração de formulário de forma incremental e se tornará mais completo à medida que você adicionar recursos ao servidor de formulários.
  
## <a name="see-also"></a>Confira também



[Conceitos de MAPI](mapi-concepts.md)

