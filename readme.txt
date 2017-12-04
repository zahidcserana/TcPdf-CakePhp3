1. store 'tecnickcom' to vendor
2. store 'pdf_view.ctp' to Template/Element
3. call the Function pdfBuild() from Your Controller

public function pdfBuild(){
        $this->viewBuilder()->layout('ajax');
        $this->set('ctp', 'file_name');  // put your ctp file name
        $this->response->type('pdf');
        $this->render('/Element/pdf_view');
    }