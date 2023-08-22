resource "local_file" "pe" {
  filename=var.filename
  content = "${random_password.name.result}"
}

resource "null_resource" "local_exec_example" {
  provisioner "local-exec" {
    command = " sudo su"
    working_dir = "/home/moh/ter/"
  }
}

resource random_password name {
  length = 10
  upper=true
  lower=true
  number=true
  special=true
  keepers={
    id=5
  }
}

output print_pass {
  value = random_password.name.result
  sensitive=true
  description = "description passwordd"
  depends_on=[]
}
