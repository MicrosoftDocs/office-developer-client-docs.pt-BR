---
title: Trabalhar com assinaturas digitais usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- assinaturas digitais [infopath 2007], modelos de formulário compatíveis com 2003 do infopath, modelos de formulário compatíveis com o InfoPath 2003, assinaturas digitais
localization_priority: Normal
ms.assetid: d6318238-fd45-4854-a3c9-c27c5685bd6b
description: O modelo de objeto compatível com o InfoPath 2003 fornece recursos para trabalhando de maneira programática com assinaturas digitais.
ms.openlocfilehash: ae9934e36766b7e783d1404a12a49e9b0b08543a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765626"
---
# <a name="work-with-digital-signatures-using-the-infopath-2003-object-model"></a>Trabalhar com assinaturas digitais usando o modelo de objeto do InfoPath 2003

O modelo de objeto compatível com o InfoPath 2003 fornece recursos para trabalhando de maneira programática com assinaturas digitais.
  
## <a name="digital-signature-features"></a>Recursos de assinatura digital

Os recursos de assinaturas digitais disponíveis no InfoPath permitem: 
  
- Ativar as assinaturas para o formulário inteiro, ou para conjuntos de dados no formato que pode ser conectado separadamente específicos.
    
- Especifica, para cada conjunto de dados que podem ser assinados, se são permitidas várias assinaturas ou uma única assinatura e quais serão elas se relacionam. Por exemplo, você pode especificar estarem ou assinaturas colegas paralelas ou se cada nova assinatura countersigns todas as assinaturas anteriores.
    
- Especifica uma mensagem a ser mostrada para os usuários do formulário como eles assinem o formulário.
    
- Inserir e ver uma assinatura do documento. 
    
- Modo de exibição não repúdio informações verificáveis que foi adicionadas para cada assinatura para aumentar a segurança. Essas informações adicionais, que inclui um modo de exibição do formulário como ela foi apresentada para cada signatário, é parte da assinatura e não podem ser removidas sem invalidar a assinatura. A qualquer momento, você pode recuperar esses dados clicando na assinatura do formulário para exibir a caixa de diálogo **Verificar Assinatura Digital** . 
    
- Beneficie-se de um modelo de objeto para trabalhar com assinaturas digitais. Adicione informações personalizadas para o bloco de assinatura em formulários totalmente confiáveis através do modelo de objeto de assinatura digital. 
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Visão geral do modelo de objeto de assinaturas digitais

### <a name="events"></a>Events

O modelo de objeto para assinaturas digitais fornece o evento a seguir.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Ocorre depois que um conjunto de dados assinados foi selecionado para fazer logon.  <br/> Você pode usar esse evento para manipular os dados armazenados em assinaturas digitais. Por exemplo, você pode adicionar dados a partir de um servidor de carimbo de hora confiável, ou adicionar uma referenda no servidor da transação. Você também pode usar esse evento para bloquear a assinatura se o usuário atual não for membro de um grupo específico.  <br/> |
   
O evento **OnSign** retorna uma referência ao objeto [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) , que fornece as seguintes propriedades. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.ReturnStatus.aspx) <br/> |Obtém ou define um valor **Boolean** que indica o status de retorno do evento **OnSign** .  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.SignedDataBlock.aspx) <br/> |Obtém o bloco de dados assinados que acionou o evento **OnSign** .  <br/> |
|[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.XDocument.aspx) <br/> |Obtém uma referência ao objeto **XDocument** associada ao evento **OnSign** .  <br/> |
   
### <a name="collections-and-objects"></a>Objetos e coleções

O modelo de objeto para assinaturas digitais fornece as seguintes coleções.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[SignedDataBlocksCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlocksCollection.aspx) <br/> |A coleção dos objetos [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) no modelo de formulário, como definido no arquivo de definição de formulário (. xsf).  <br/> A coleção de **SignedDataBlocksCollection** implementa propriedades que podem ser usadas para acessar os objetos **SignedDataBlockObjects** associados a um formulário. **O pode ser acessada por meio da propriedade [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) do objeto [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) .**  <br/> |
|[SignaturesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignaturesCollection.aspx) <br/> |Contém uma coleção de objetos [SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) para cada **SignedDataBlockObject** no formulário.  <br/> A coleção de **SignaturesCollection** implementa propriedades e um método que pode ser usado para acessar objetos **SignatureObject** associados a um formulário e criar uma assinatura. Ele é acessível através do objeto **SignedDataBlockObject** .  <br/> Quando você usa o método [Create](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) da coleção **SignaturesCollection** , mantenha em mente que a assinatura não é gravada até o [sinal de](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) método é chamado no objeto **SignatureObject** . Esses métodos podem ser chamados somente do manipulador de eventos **OnSign** de um modelo de formulário totalmente confiável.  <br/> |
   
O modelo de objeto para assinaturas digitais fornece os seguintes objetos.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) <br/> |Representa um conjunto de dados assinados em um formulário. O objeto **SignedDataBlock** fornece um número de propriedades e um método que pode ser usado para interagir programaticamente com um conjunto de dados assinados.  <br/> |
|[SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) <br/> |Representa uma assinatura digital que foi adicionada a um formulário ou um conjunto de dados assinados em um formulário. A coleção de **SignatureObject** implementa propriedades que podem ser usadas para recuperar informações sobre a assinatura digital e o método de [entrada](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) para escrever o bloco de assinatura digital XML e seu valor de hash criptográfico de computação.  <br/> |
|[CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) <br/> |Representa o certificado digital x. 509 que foi usado para criar a assinatura.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Trabalhando de maneira programática com assinaturas digitais

O modelo de objeto compatível com o InfoPath 2003 fornece membros para interação com assinaturas digitais programaticamente. Em particular, formulários totalmente confiáveis podem adicionar informações personalizadas para o bloco de assinatura antes que ele seja confirmado, de acordo com a seguinte linha de tempo:
  
1. Usuário optar por adicionar uma assinatura digital a um formulário.
    
2. O primeiro painel do **Assistente de Assinatura Digital** é exibido. 
    
3. O evento **OnSign** para os dados selecionados representados pelo objeto **SignedDataBlockObject** é gerado e o método de **entrada** do **SignedDataBlockObject** e o método **Create** do **SignaturesCollection** coleção são executados. 
    
4. Quaisquer ações personalizadas opcionais são executadas.
    
5. O método de **entrada** do **SignatureObject** é executado. 
    
6. Painéis de segundo e terceiro do assistente são exibidos para selecionar um certificado para assinar com e insira comentários.
    
7. As informações de não-recusa são exibidas (que podem ser exibidos posteriormente com a caixa de diálogo **Verificar Assinatura Digital** ). 
    
8. Quando o botão de **entrada** é clicado, a assinatura é adicionada à coleção de assinaturas para o formulário. 
    
O exemplo a seguir invoca a caixa de diálogo de **logon** e countersigns a assinatura com um valor de carimbo de hora é recuperada de um serviço de carimbo de hora confiável. 
  
```cs
[InfoPathEventHandler(EventType=InfoPathEventType.OnSign)]
public void OnSign(SignEvent e)
{
    Signature signature = e.SignedDataBlock.Signatures.Create();
    // Invoke the Sign dialog box to sign the data block.
    signature.Sign();
    // Countersign the signature with a trusted timestamp
    // Get the XML node storing the signature block
    IXMLDOMNode oNodeSig = signature.SignatureBlockXmlNode;
    IXMLDOMNode oNodeSigValue = oNodeSig.selectSingleNode(".//*[local-name(.)='signatureValue']");
    // Get timestamp from a trusted timestamp service (fictitious).
    MyTrustedTimeStampService s = new MyTrustedTimeStampService();
    string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.text);
    
    //Add the value returned from the timestamp service to the 
    //unsigned part of the signature block
    IXMLDOMNode oNodeObj = oNodeSig.selectSingleNode(".//*[local-name(.)='Object']");
    IXMLDOMNode oNode = oNodeObj.cloneNode(false);
    oNode.text = strVerifiedTimeStamp;
    oNodeObj.parentNode.appendChild(oNode);
    e.ReturnStatus = true;
}
```


