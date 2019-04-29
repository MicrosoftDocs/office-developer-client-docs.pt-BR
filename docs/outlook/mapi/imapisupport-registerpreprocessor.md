---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 58215de6cc4e9e68386f8f017839752acc6e1753
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404894"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra a função de pré-processador de um provedor de transporte (uma função que está em conformidade com o protótipo [PreprocessMessage](preprocessmessage.md) ). 
  
```cpp
HRESULT RegisterPreprocessor(
LPMAPIUID lpMuid,
LPSTR lpszAdrType,
LPSTR lpszDLLName,
LPSTR lpszPreprocess,
LPSTR lpszRemovePreprocessInfo,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpMuid_
  
> no Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador que a função de pré-processador manipula. O parâmetro _lpMuid_ pode ser NULL. 
    
 _lpszAdrType_
  
> no Um ponteiro para o tipo de endereço das mensagens que a função Opera, como FAX, SMTP ou X500. O parâmetro _lpszAdrType_ pode ser NULL. 
    
 _lpszDLLName_
  
> no Um ponteiro para o nome da biblioteca de vínculo dinâmico (DLL) que contém o ponto de entrada para a função de pré-processador.
    
 _lpszPreprocess_
  
> no Um ponteiro para o nome da função de pré-processador. O parâmetro _lpszPreprocess_ pode ser NULL. 
    
 _lpszRemovePreprocessInfo_
  
> no Um ponteiro para o nome da função que remove as informações do pré-processador (uma função que está de acordo com o protótipo do [RemovePreprocessInfo](removepreprocessinfo.md) ). O parâmetro _lpszRemovePreprocessInfo_ pode ser NULL. 
    
 _ulFlags_
  
> Serve deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A função de pré-processador foi registrada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: RegisterPreprocessor** é implementado apenas para objetos de suporte do provedor de transporte. Os provedores de transporte chamam **RegisterPreprocessor** para registrar uma função de pré-processador (uma função que está em conformidade com o protótipo do [PreprocessMessage](preprocessmessage.md) ). Uma função de pré-processador deve ser registrada antes que o spooler MAPI possa chamá-lo. 
  
Os parâmetros _lpszPreprocess_, _lpszRemovePreprocessInfo_e _lpszDLLName_ devem apontar para cadeias de caracteres que podem ser usadas em conjunto com as chamadas para a função de **GetProcAddress** do Win32, permitindo a DLL do pré-processador ponto de entrada a ser chamado corretamente. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

As chamadas para pré-processadors são específicas para a ordem do provedor de transporte. Isso significa que, se outro provedor de transporte antes do seu provedor puder lidar com uma mensagem, sua função de pré-processador não será chamada para essa mensagem. Sua função de pré-processador será chamada somente para mensagens que você manipulará.
  
Você pode escrever funções de pré-processador para lidar com um identificador específico armazenado em uma estrutura [MAPIUID](mapiuid.md) ou um tipo de endereço. Se você especificar uma estrutura **MAPIUID** no parâmetro _lpMuid_ e um tipo de endereço no parâmetro _lpszAdrType_ , sua função será chamada para destinatários de mensagens que correspondam ao **MAPIUID** ou ao tipo de endereço. Se _lpMuid_ for nulo e _LPSZADRTYPE_ for não nulo, sua função será chamada somente para destinatários que tenham um endereço que corresponda ao tipo apontado por _lpszAdrType_. Se _lpMuid_ for não nulo e _lpszAdrType_ for nulo, sua função será chamada para destinatários que correspondam a **MAPIUID**, independentemente do tipo de endereço. Se ambos forem nulos, sua função será chamada para todos os destinatários da mensagem.
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

