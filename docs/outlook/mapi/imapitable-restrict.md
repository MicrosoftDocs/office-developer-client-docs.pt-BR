---
title: IMAPITableRestrict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Restrict
api_type:
- COM
ms.assetid: a5bfc190-b58f-44c3-893c-8727df14ee58
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6cca6bc12fa6f100885b7bf705d79fa24a2e2f91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414617"
---
# <a name="imapitablerestrict"></a>IMAPITable::Restrict

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aplica um filtro a uma tabela, reduzindo o conjunto de linhas somente para as linhas que correspondam aos critérios especificados.
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpRestriction_
  
> no Ponteiro para uma estrutura [SRestriction](srestriction.md) que define as condições do filtro. Passar NULL no parâmetro _lpRestriction_ remove o filtro atual. 
    
 _ulFlags_
  
> no Bitmask de sinalizadores que controla o intervalo da operação de restrição. Os seguintes sinalizadores podem ser definidos:
    
TBL_ASYNC 
  
> Inicia a operação de forma assíncrona e retorna antes de a operação ser concluída.
    
TBL_BATCH 
  
> Adia a avaliação do filtro até que os dados na tabela sejam necessários.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O filtro foi aplicado com êxito.
    
MAPI_E_BUSY 
  
> Há outra operação em andamento que impede a inicialização da operação de restrição. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
MAPI_E_TOO_COMPLEX 
  
> A tabela não pode executar a operação porque o filtro específico apontado pelo parâmetro _lpRestriction_ é muito complicado. 
    
## <a name="remarks"></a>Comentários

O método imApitable **:: Restrict** estabelece uma restrição ou um filtro em uma tabela. Se houver uma restrição anterior, ela será descartada e a nova aplicada. A aplicação de uma restrição não afeta os dados subjacentes de uma tabela; Ele simplesmente altera o modo de exibição, limitando as linhas que podem ser recuperadas em linhas que contenham dados que satisfaçam a restrição. 
  
Há vários tipos diferentes de restrições, cada um descrito com uma estrutura diferente. A estrutura [SRestriction](srestriction.md) contém dois membros: um valor que indica o tipo de restrição e a estrutura específica aplicável a esse tipo. 
  
As notificações para linhas de tabela que estão ocultas de modo de exibição por chamadas ao **restringir** nunca são geradas. 
  
Uma restrição de propriedade em uma propriedade de vários valores funciona como uma restrição em uma propriedade de valor único. Uma propriedade de vários valores a ser usada em uma restrição de propriedade deve ter o sinalizador MVI_FLAG definido. Se não houver esse sinalizador definido, ele será tratado como uma tupla totalmente ordenada. Uma comparação de duas colunas com vários valores compara os elementos de coluna em ordem, relatando a relação das colunas na primeira inequação. A igualdade é retornada somente se as colunas comparadas contiverem os mesmos valores na mesma ordem. Se uma coluna tiver menos valores do que o outro, a relação relatada será a de um valor nulo para o outro valor.
  
Para obter mais informações sobre restrições, consulte [about Restrictions](about-restrictions.md).
  
> [!NOTE]
> Se você criar consultas dinâmicas para pesquisar dados no servidor, use o método **FindRow** em vez de usar o **** método restrict e o método **QueryRows** juntos. O **** método restrict cria um modo de exibição em cache que é usado para avaliar todas as mensagens adicionadas ou modificadas na pasta base. Se um aplicativo cliente usar o **** método restrict para cada consulta dinâmica, um modo de exibição em cache será criado para cada consulta. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para descartar a restrição atual sem criar uma nova, passe NULL no _lpRestriction_.
  
Se outra chamada de tabela assíncrona estiver em andamento, fazendo com que o **limite** retorne MAPI_E_BUSY, você poderá chamar IMAPITable [:: Abort](imapitable-abort.md) para interromper a chamada. 
  
 **** O restrict funciona de forma síncrona, a menos que você defina um dos sinalizadores. Se você definir o sinalizador TBL_BATCH, **restrict** adia a avaliação da restrição, a menos que você solicite os dados. Se o sinalizador TBL_ASYNC estiver definido, o **restringir**funciona de forma assíncrona, potencialmente retornando antes da conclusão da operação.
  
Todos os indicadores de uma tabela são descartados quando uma chamada para **restrict** é feita, e BOOKMARK_CURRENT, a posição atual do cursor, é definida como o início da tabela. 
  
Se você tentar impor uma restrição de propriedade em uma propriedade que não esteja no conjunto de colunas da tabela, os resultados serão indefinidos. Sempre que você não tiver certeza sobre se uma propriedade é suportada em uma tabela, combine a restrição de propriedade com uma restrição Exists. A restrição Exists verifica a existência da propriedade antes de tentar impor a restrição de propriedade. 
  
Não espera receber uma notificação de tabela em uma linha que tenha sido filtrada de uma tabela devido a uma restrição.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl:: ApplyRestriction  <br/> |MFCMAPI usa o método imApitable **:: Restrict** para definir uma restrição em uma tabela.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::ExpandRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

