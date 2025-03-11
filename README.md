# distribute-ssh-keys# distribute-ssh-keys

This repository contains an Ansible playbook to distribute SSH public keys to all hosts.

## Files

- `deploy_ssh_keys.yaml`: Ansible playbook to distribute SSH public keys.

## Usage

1. Ensure you have Ansible installed on your control machine.
2. Update the `deploy_ssh_keys.yaml` file if necessary.
3. Run the playbook with the following command:

    ```sh
    ansible-playbook -i <inventory_file> deploy_ssh_keys.yaml
    ```

    Replace `<inventory_file>` with your Ansible inventory file.

## Playbook Details

- **Playbook Name**: Distribute SSH public keys
- **Hosts**: all
- **Gather Facts**: false

### Tasks

1. **Ensure .ssh directory exists**:
    - Creates the `.ssh` directory in the user's home directory with `0700` permissions.

2. **Copy public SSH key to authorized_keys**:
    - Copies the specified public SSH key to the `authorized_keys` file for the user.

## License

This project is licensed under the MIT License.