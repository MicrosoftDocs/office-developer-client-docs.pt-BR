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
ms.openlocfilehash: b5902c25197c2ae5790e654a8f29227e107b4a72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768158"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

  
  
**Aplica-se a**: Outlook 
  
Função de ponto de entrada de serviço de mensagem para um MAPI armazenar provedor para empacotar um repositório local baseado em PST como um repositório NST. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Implementada por:  <br/> |Provedor MAPI  <br/> |
|Chamado pelo:  <br/> |MAPI  <br/> |
   
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

 **NSTServiceEntry** usa o protótipo de função **[MSGSERVICEENTRY](msgserviceentry.md)** . Para obter informações sobre seus parâmetros, consulte **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="return-values"></a>Valores de retorno

Para obter informações sobre valores de retorno, consulte **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="remarks"></a>Comentários

Ao usar o **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** para procurar o endereço desta função no Msmapi32, especifique "NSTServiceEntry" como o nome do procedimento. 
  
Para usar a API de replicação, um provedor de repositório MAPI deve primeiro abrir e quebrar um repositório local baseado em PST chamando **[NSTServiceEntry](nstserviceentry.md)**. O provedor, em seguida, pode usar as interfaces principais da API, **[IOSTX](iostxiunknown.md)** e **[IPSTX](ipstxiunknown.md)**, para realizar a replicação. 
  
Os comentários a seguir se aplicam a um repositório NST:
  
- Não armazene qualquer informação na seção perfil global ao implementar um provedor MAPI que usa **NSTServiceEntry**. A seção perfil global é compartilhada por vários provedores e dados armazenados neste perfil podem ser substituídos. 
    
- Somente os itens cujo existente carimbos de hora de modificação obtém seus carimbos atualizados quando elas forem salvas. 
    
- Verificação de conflito não ocorre automaticamente quando itens são salvos.
    
-  Detecção de duplicatas não ocorrerá quando os itens são salvos. 
    
-  O arquivo que representa a versão em cache do servidor é acrescentado com. NST. 
    
- Para obter um ponteiro para a seção perfil global, um serviço de mensagem chama **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** no objeto suporte usando **pbNSTGlobalProfileSectionGuid** , conforme definido abaixo: 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- Nesse caso, o objeto de suporte do serviço de mensagem deve assegurar que **IMAPISupport::OpenProfileSection** retorna a seção de perfil que é identificada pela propriedade **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** na seção perfil padrão. Para fazer esta seção de perfil, o objeto de suporte pode abrir a seção de perfil padrão, recuperar **PR_SERVICE_UID**e passar o resultado para **IMAPISupport::OpenProfileSection** para recuperar a seção de perfil global correto. Por sua vez, o objeto de suporte retorna um ponteiro para esta seção perfil global para o serviço de mensagem. 
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)

