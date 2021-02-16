---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 96c04a242c477204ea1447fb78c31d189eeac59a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280051"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Função de ponto de entrada do serviço de mensagens para um provedor de armazenamento MAPI quebrar um armazenamento local baseado em PST como um armazenamento NST. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Implementado por:  <br/> |Provedor MAPI  <br/> |
|Chamado por:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT NSTServiceEntry( 
    HINSTANCE hInstance,   
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR * lppMapiError 
);
```

## <a name="parameters"></a>Parâmetros

 **NSTServiceEntry** usa o protótipo **[de função MSGSERVICEENTRY.](msgserviceentry.md)** Para obter informações sobre seus parâmetros, consulte **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="return-values"></a>Valor de retorno

Para obter informações sobre valores de retorno, consulte **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="remarks"></a>Comentários

Ao usar **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** para procurar o endereço dessa função no msmapi32.dll, especifique "NSTServiceEntry" como o nome do procedimento. 
  
Para usar a API de replicação, um provedor de armazenamento MAPI deve primeiro abrir e quebrar um armazenamento local baseado em PST chamando **[NSTServiceEntry](nstserviceentry.md)**. Em seguida, o provedor pode usar as principais interfaces da API, **[IOSTX](iostxiunknown.md)** e **[IPSTX](ipstxiunknown.md)** para realizar a replicação. 
  
Os comentários a seguir se aplicam a um armazenamento NST:
  
- Não armazene nenhuma informação na seção de perfil global ao implementar um provedor MAPI que usa **NSTServiceEntry**. A seção de perfil global é compartilhada por muitos provedores e os dados armazenados nesse perfil podem ser substituídos. 
    
- Somente os itens com carimbos de data/hora de modificação existentes têm seus carimbos atualizados quando são salvos. 
    
- A verificação de conflitos não ocorre automaticamente quando os itens são salvos.
    
-  A detecção duplicada não ocorre quando os itens são salvos. 
    
-  O arquivo que representa a versão em cache do servidor é anexado a . NST. 
    
- Para obter um ponteiro para a seção de perfil global, um serviço de mensagens chama **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** no objeto de suporte usando **pbNSTGlobalProfileSectionGuid** conforme definido abaixo: 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- Nesse caso, o objeto de suporte do serviço de mensagens deve garantir que **IMAPISupport::OpenProfileSection** retorne a seção de perfil identificada pela propriedade **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** na seção de perfil padrão. Para obter esta seção de perfil, o objeto de suporte pode abrir a seção de perfil padrão, recuperar **PR_SERVICE_UID** e passar o resultado para **IMAPISupport::OpenProfileSection** para recuperar a seção de perfil global correta. O objeto de suporte, por sua vez, retorna um ponteiro para essa seção de perfil global para o serviço de mensagens. 
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)

