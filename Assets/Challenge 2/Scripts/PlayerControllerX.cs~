using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerControllerX : MonoBehaviour
{
    public GameObject dogPrefab;

    private bool isShoot = true;

    // Update is called once per frame
    void Update()
    {
        // On spacebar press, send dog
        if (Input.GetKeyDown(KeyCode.Space) && isShoot)
        {
            Instantiate(dogPrefab, transform.position, dogPrefab.transform.rotation);
            StartCoroutine("Reload");
        }
    }

    IEnumerator Reload() {
        isShoot = false;
        yield return new WaitForSeconds(1.0f);
        isShoot = true;
    }
}
