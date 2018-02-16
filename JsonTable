<?php

/**
 * Created by: Den
 * admin@whileweb.com
 * Date: 16.02.2018
 * Time: 21:02:40
 */
class JsonTable
{
    public static function render(array $data, array $options = [])
    {
        if(!is_array($data)) return '';

        $attrStr = '';

        if(isset($options['attr']))
        {
            if(is_array($options['attr']))
            {
                foreach ($options['attr'] as $attrName => $attrVal)
                {
                    $attrStr .= $attrName . '="' . $attrVal . '" ';
                }
            }
        }

        $html = "<table $attrStr>";

        foreach ($data as $key => $val)
        {
            if(is_string($val))
            {
                $html .= "<tr><td>$key</td><td>$val</td></tr>";
            }
            elseif (is_array($val))
            {
                $html .= "<tr><td>$key</td><td>" . self::render($val, $options) . "</td></tr>";
            }
        }
        $html .= '</table>';

        return $html;
    }
}
