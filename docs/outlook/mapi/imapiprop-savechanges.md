---
title: IMAPIPropSaveChanges
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SaveChanges
api_type:
- COM
ms.assetid: 864dbc3e-2039-435a-a279-385d79d1d13f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2c8244180a5cafedc887fa72f36f233fb5084f79
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398840"
---
# <a name="imapipropsavechanges"></a>IMAPIProp::SaveChanges

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Torna permanente quaisquer alterações feitas a um objeto desde a última operação de salvamento. 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o que acontece ao objeto quando o método **IMAPIProp::SaveChanges** é chamado. Sinalizadores a seguir podem ser definidos: 
    
NON_EMS_XP_SAVE
  
> Indica que a mensagem não foi entregue a partir de um Microsoft Exchange Server. Esse sinalizador deve ser usado em conjunto com o método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) e o sinalizador ITEMPROC_FORCE para indicar um repositório PST que a mensagem é qualificada para regras de processamento antes que o repositório de arquivos (. PST) de pastas particulares notifica qualquer um cliente de escuta que a mensagem foi entregue. Este regras processamento só se aplica às novas mensagens que são criadas com [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) em um servidor que não seja um servidor do Exchange, caso em que o Exchange Server seriam já processados regras na mensagem. 
    
FORCE_SAVE 
  
> As alterações devem ser gravadas no objeto, substituindo quaisquer alterações anteriores que foram feitas ao objeto, e o objeto deve ser fechado. Permissão de leitura/gravação deve ser definida para a operação tenha êxito. O sinalizador FORCE_SAVE é usado após uma chamada anterior para **SaveChanges** retornado MAPI_E_OBJECT_CHANGED. 
    
KEEP_OPEN_READONLY 
  
> As alterações devem ser confirmadas e o objeto deve ser mantido aberto para leitura. Nenhuma alteração adicional será feita. 
    
KEEP_OPEN_READWRITE 
  
> As alterações devem ser confirmadas e o objeto deve ser mantido aberto para permissão de leitura/gravação. Esse sinalizador geralmente é definido quando o objeto foi aberto pela primeira vez para permissão de leitura/gravação. As alterações subsequentes ao objeto são permitidas. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite **SaveChanges** retornar com êxito, possivelmente antes que as alterações forem confirmadas totalmente. 
    
SPAMFILTER_ONSAVE
  
> Permite que o spam filtrados em uma mensagem que está sendo salva. O suporte à filtragem de spam está disponível somente se o tipo de endereço de email do remetente for SMTP(Simple Mail Transfer Protocol) e a mensagem estiver sendo salva em um repositório de um arquivo de pastas particulares (PST).
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O compromisso de alterações foi bem-sucedida.
    
MAPI_E_NO_ACCESS 
  
> **SaveChanges** não podem manter o objeto aberto para permissão somente leitura se KEEP_OPEN_READONLY for definido, ou permissão de leitura/gravação, se KEEP_OPEN_READWRITE estiver definida. Sem alterações são confirmadas. 
    
MAPI_E_OBJECT_CHANGED 
  
> O objeto foi alterado desde que foi aberto.
    
MAPI_E_OBJECT_DELETED 
  
> O objeto foi excluído desde que ela foi aberta.
    
## <a name="remarks"></a>Comentários

O método **IMAPIProp::SaveChanges** faz com que as alterações de propriedade permanente para objetos que suportam o modelo de transação do processamento, como mensagens, anexos, recipientes do catálogo de endereços e objetos de usuário de mensagens. Objetos que não oferecem suporte a transações, como pastas, repositórios de mensagem e seções de perfil, faça alterações permanentes imediatamente. Nenhuma chamada para **SaveChanges** é necessária. 
  
Porque não têm os provedores de serviço gerar um identificador de entrada para seus objetos até que todas as propriedades foram salvos, **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) propriedade de um objeto pode não estar disponível até após seu método **SaveChanges** foi chamado. Alguns provedores de aguardar até que o sinalizador KEEP_OPEN_READONLY está definido na chamada **SaveChanges** . KEEP_OPEN_READONLY indica que as alterações sejam salvos na chamada atual será as últimas alterações serão feitas no objeto. 
  
Algumas implementações de repositório de mensagem do não mostrar recém-criadas mensagens em uma pasta até que um cliente salva a mensagem altera usando **SaveChanges** e libera os objetos de mensagem usando o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . Além disso, algumas implementações de objeto não é possível gerar uma propriedade **PR_ENTRYID** para um objeto recém-criado até depois **SaveChanges** foi chamado e alguns podem fazê-lo apenas depois **SaveChanges** tiver sido chamado usando KEEP_OPEN_READONLY Defina no _ulFlags_.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se você receber o sinalizador KEEP_OPEN_READONLY, você tem a opção de deixar o acesso do objeto como leitura/gravação. No entanto, um provedor pode nunca deixe um objeto em um estado somente leitura quando o sinalizador KEEP_OPEN_READWRITE é passado.
  
Quando um cliente salva vários anexos para várias mensagens, ele chama o método **SaveChanges** para cada anexo e cada mensagem. Geralmente, clientes definirão MAPI_DEFERRED_ERRORS para cada uma dessas chamadas, exceto o último. Você pode retornar erros com a última chamada ou chamadas anteriores. Você pode até mesmo ignorar o sinalizador. 
  
Se KEEP_OPEN_READWRITE ou KEEP_OPEN_READONLY for definido em conjunto com MAPI_DEFERRED_ERRORS, você pode ignorar a solicitação de diferimento de erro. Se MAPI_DEFERRED_ERRORS não estiver definida no _ulFlags_, um dos erros adiados anteriormente pode ser retornado para a chamada **SaveChanges** . 
  
Se um provedor de transporte remoto fornece uma implementação funcional deste método é opcional e depende de outras escolhas de design na sua implementação. Se você implementar esse método, fazê-lo de acordo com a documentação aqui. Porque os objetos de pasta e objetos de status não serão transacionados, no mínimo implementação do provedor de um transporte remoto **SaveChanges** deve retornar S_OK sem realmente fazer qualquer trabalho. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se um cliente passa KEEP_OPEN_READONLY, chama o método [IMAPIProp::SetProps](imapiprop-setprops.md) e, em seguida, chama **SaveChanges** novamente, a mesma implementação pode falhar. 
  
Após receber MAPI_E_NO_ACCESS de uma chamada no qual você definiu KEEP_OPEN_READWRITE, continuará a ter permissão de leitura/gravação para o objeto. É possível chamar **SaveChanges** novamente, passando o sinalizador KEEP_OPEN_READONLY ou sem sinalizadores com KEEP_OPEN_SUFFIX. 
  
Se um provedor suporta o sinalizador KEEP_OPEN_READWRITE depende da implementação do provedor. 
  
Para indicar que a chamada apenas ser feitas no objeto após **SaveChanges** é **IUnknown:: Release**, não defina nenhum sinalizadores para o parâmetro _ulFlags_ . Um erro de **SaveChanges** indica que ele não pôde tornar as alterações pendentes permanente. Provedores diferentes manipulam a ausência de sinalizadores na chamada **SaveChanges** de forma diferente. Alguns provedores tratam nesse estado da mesma forma KEEP_OPEN_READONLY; outros provedores interpretam o mesmo KEEP_OPEN_READWRITE. Ainda outros provedores desligar o objeto quando não recebem sinalizadores na chamada **SaveChanges** . 
  
Algumas propriedades, normalmente computadas propriedades, não podem ser processadas até que se chame **SaveChanges** e, em alguns casos, a **versão**.
  
Quando você faz alterações em massa, como salvar anexos de várias mensagens, adie o erro de processamento, definindo o sinalizador MAPI_DEFERRED_ERRORS no _ulFlags_. Se você salvar vários anexos para várias mensagens, fazer um **SaveChanges** chamada para cada anexo e um **SaveChanges** chamada a cada mensagem. Defina o sinalizador MAPI_DEFERRED_ERRORS para cada chamada de anexo e para todas as mensagens, exceto o último. 
  
Se **SaveChanges** retornar MAPI_E_OBJECT_CHANGED, verifique se o objeto original foi modificado. Em caso afirmativo, avise o usuário, que pode solicitar que as alterações sobrescrever as alterações anteriores ou salvar o objeto em outro local. Se o objeto original tiver sido excluído, avise o usuário para fornecer-lhes a oportunidade de salvar o objeto em outro local. 
  
Você não pode chamar **SaveChanges** com o sinalizador FORCE_SAVE em um objeto aberto que tenha sido excluído. 
  
Se **SaveChanges** retornará um erro, o objeto cujas alterações foram salvos permanece aberto, independentemente dos sinalizadores definidos no parâmetro _ulFlags_ . 
  
> [!IMPORTANT]
> O _ulFlags_ NON_EMS_XP_SAVE e SPAMFILTER_ONSAVE não podem ser definidos no arquivo de cabeçalho para download que você possui atualmente, nesse caso, você pode adicioná-lo ao seu código usando os seguintes valores: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
Para obter mais informações, consulte [Salvar Propriedades de MAPI](saving-mapi-properties.md).
  
## <a name="see-also"></a>Confira também



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[Propriedade canônico PidTagEntryId](pidtagentryid-canonical-property.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Salvar propriedades MAPI](saving-mapi-properties.md)

