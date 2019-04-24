---
title: Armazenamento estruturado no MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f58fa70e98841db5507323a63737f1df6c1b7a6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327430"
---
# <a name="structured-storage-in-mapi"></a>Armazenamento estruturado no MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O armazenamento estruturado refere-se à organização hierárquica do armazenamento introduzida com o COM. Em um ambiente de armazenamento estruturado, o armazenamento é organizado em dois ou três tipos de objetos: 
  
- Objetos Stream
    
- Objetos de bloqueio bytes
    
- Objetos de armazenamento
    
Bytes de fluxo e bloqueio são objetos de nível inferior que acessam diretamente os dados. Os objetos Stream implementam a interface **IStream** que define métodos para leitura, gravação, posicionamento e cópia de bytes de dados. Os objetos Lock bytes implementam outra interface COM, **ILockBytes**, para acessar dados com uma matriz de bytes. Geralmente, as matrizes de bytes são usadas para fornecer acesso personalizado ao armazenamento subjacente.
  
Os objetos de armazenamento são em camadas na parte superior dos objetos Stream ou Lock bytes; Eles podem conter um ou mais desses objetos, bem como outros objetos de armazenamento. Os objetos de armazenamento implementam a interface **IStorage** que define métodos para criar, acessar e manter objetos aninhados. 
  
Como **IStream**, **ILockBytes**e **IStorage** são interfaces com em vez de interfaces MAPI, seus métodos retornam valores de erro com em vez de valores MAPI. Os métodos de chamada de provedores de clientes e de serviços nessas interfaces devem usar a função de API **MapStorageSCode** para converter esses valores em valores de erro MAPI. Para obter mais informações, consulte [MapStorageSCode](mapstoragescode.md).
  
Os clientes e provedores de serviços usam o armazenamento estruturado para trabalhar com propriedades que são muito grandes para serem mantidas com os métodos **IMAPIProp** , geralmente cadeias de caracteres e propriedades binárias. Uma das maneiras comuns de os clientes ou provedores de serviços acessá-los, especificando **IStream** ou **IStorage** como o identificador de interface em uma chamada para o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) . Por exemplo, os clientes **** chamam OpenProperty com **PR_ATTACH_DATA_BIN** como a marca de propriedade e IID_IStream como o identificador de interface para acessar um anexo binário em uma mensagem. 
  
Os clientes e provedores de serviços podem implementar seus próprios objetos Stream e de armazenamento ou as funções da API de chamada para acessar as implementações fornecidas pelo MAPI ou COM. Como as implementações fornecidas atendem a maioria dos fins, os clientes e provedores de serviço raramente precisam criar seus próprios. 
  
Quando um cliente chama **OpenProperty** em um objeto MAPI para acessar uma de suas propriedades por meio de um objeto de armazenamento, o provedor de serviços normalmente abre o objeto de armazenamento no modo direto. No enTanto, isso é típico, e não o comportamento necessário. Os clientes devem supor que todos os objetos de armazenamento abertos ou criados por provedores de serviço sejam transacionados e exijam uma chamada para **IStorage:: Commit**. Eles também devem se lembrar de que as alterações nos objetos de armazenamento não serão permanentes até chamar **IMAPIProp:: SaveChanges** após a **confirmação** final para salvar o objeto MAPI. Para obter mais informações, consulte [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).
  
MAPI e COM fornecem várias funções de API para definir ou acessar objetos de armazenamento e Stream. As funções comumente usadas são descritas na tabela a seguir.
  
**Funções para acessar objetos de armazenamento e Stream**

|**Function**|**Descrição**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Cria um objeto de armazenamento para acessar um objeto Stream ou Lock bytes.  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Cria um objeto de mensagem para acessar um objeto de armazenamento.  <br/> |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |Cria um objeto Stream para acessar um arquivo.  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Cria um objeto Stream que contém a versão compactada ou descompactada de um fluxo contendo o Rich Text de uma mensagem.  <br/> |
   
 **Para recuperar os nomes dos fluxos em um determinado subarmazenamento**
  
1. Chame o método **IStorage:: EnumElements** do subarmazenamento para obter uma interface **IEnumSTATSTG** . 
    
2. Chamar **IEnumSTATSTG:: próximo** com tantas estruturas **STATSTG** de cada vez, como você pode. Se você solicitar 100 por vez, **em seguida** , normalmente retornará S_FALSE com o conteúdo do _pceltFetched_ definido para o número que foi realmente recuperado. 
    
3. Verifique as estruturas **STATSTG** sinalizadas com STGTY_STREAM. 
    
4. Libere o parâmetro _pwcsName_ . 
    
 **Para criar um objeto de armazenamento para acessar um objeto Stream ou Lock bytes existente**
  
- Os clientes chamam [HrIStorageFromStream](hristoragefromstream.md). 
    
 **Para criar um objeto Message para acessar um objeto de armazenamento existente**
  
- Os provedores de serviços e clientes chamam o [OpenIMsgOnIStg](openimsgonistg.md). O objeto Message que é criado difere dos objetos Message normalmente criados por provedores de repositório de mensagens, pois ele não oferece suporte a todos os métodos de interface [IMessage: IMAPIProp](imessageimapiprop.md) , como **IMessage:: SubmitMessage**. Um parâmetro de entrada opcional para **OpenIMsgOnIStg** é uma função de retorno de chamada que está em conformidade com o protótipo [MSGCALLRELEASE](msgcallrelease.md) . Essa função é chamada pelo novo objeto Message quando a contagem de referência da mensagem chega a zero. Implementar uma função **MSGCALLRELEASE** pode ser útil para executar o processamento final antes que a nova mensagem seja completamente removida. 
    
[OpenStreamOnFile](openstreamonfile.md) é comumente usado para armazenar anexos de arquivo porque ele cria um Stream que lê e grava em um arquivo. **OpenProperty** com **PR_ATTACH_DATA_BIN** como a marca de propriedade cria um fluxo para armazenar dados de anexo binário. 
  
 **Para compactar ou descompactar um fluxo contendo o texto da mensagem no formato Rich Text**
  
- Os clientes chamam [WrapCompressedRTFStream](wrapcompressedrtfstream.md). **WrapCompressedRTFStream** cria um Stream que quebra o fluxo RTF. O fluxo de conteúdo adicional não implementa todos os métodos de **IStream** ; os seguintes métodos são excluídos: **Seek**, **SetSize**, **REVERT**, **LockRegion**, **UnlockRegion**, **stat**e **clone**. Isso ocorre porque os objetos Stream criados por **WrapCompressedRTFStream** não oferecem suporte a **SetSize** ou **stat**, não há uma maneira fácil de estender ou recuperar seu tamanho. A melhor estratégia é selecionar um tamanho de buffer razoável e ler ou escrever em um loop.
    
> [!NOTE]
> COM tem uma implementação de objeto de armazenamento com base em uma matriz de bytes que retorna um objeto **IEnumSTATSTG** do método **EnumElements** que é problemático. Em particular, o método **QueryInterface** não funciona corretamente. Os provedores de serviços que implementam seus próprios objetos de armazenamento usando a implementação COM devem criar um invólucro Thin para o objeto **IEnumSTATSTG** que encaminha as chamadas para os métodos subjacentes do **IEnumSTATSTG** , mas implementa seu próprio **AddRef **, Os métodos **Release**, **QueryInterface**e **clone** . 
  

